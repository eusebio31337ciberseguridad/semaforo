list p=16f84 
     include        "p16F84A.inc"
     org               00h

;CONFIGURACION DE PUERTOS

     bsf               STATUS,5
     movlw             00h
     movwf             TRISB
    
     bcf               STATUS,5

;PROGRAMA PRINCIPAL

inicio movlw 10h
       movwf PORTB
       call  sg1    ;LLAMADA AL RETARDO
       movlw 08h
       movwf PORTB
       call  sg1
       movlw 04h
       movwf PORTB
       call  sg1
       movlw 06h
       movwf PORTB
       call  sg1
       movlw 02h
       movwf PORTB
       call  sg1
       movlw 01h
       movwf PORTB
       call  sg1
       movlw 08h
       movwf PORTB
       call  sg1
       goto  inicio

;-------------------------------------------------------------
; Generado con PDEL ver SP  r 1.0  el 05/12/2007 Hs 1:54:56
; Descripcion: Delay 3000000 ciclos
;-------------------------------------------------------------
sg1     movlw     .67       ; 1 set numero de repeticion  (C)
        movwf     0ch       ; 1 |
PLoop0  movlw     .91       ; 1 set numero de repeticion  (B)
        movwf     0dh       ; 1 |
PLoop1  movlw     .122      ; 1 set numero de repeticion  (A)
        movwf     0eh       ; 1 |
PLoop2  clrwdt              ; 1 clear watchdog
        decfsz    0eh, 1    ; 1 + (1) es el tiempo 0  ? (A)
        goto      PLoop2    ; 2 no, loop
        decfsz    0dh,  1   ; 1 + (1) es el tiempo 0  ? (B)
        goto      PLoop1    ; 2 no, loop
        decfsz    0ch,  1   ; 1 + (1) es el tiempo 0  ? (C)
        goto      PLoop0    ; 2 no, loop
PDelL1  goto PDelL2         ; 2 ciclos delay
PDelL2  clrwdt              ; 1 ciclo delay
        return              ; 2+2 Fin.
;-------------------------------------------------------------

        return

end
