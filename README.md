# lojassaulo3clenteJAVA

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.mycompany.cliente;


public class cliente {
   private String nome;
   private String email;
   private float credito;
   
   public cliente(String nome,String email,float credito){
       this.nome = nome;
       this.email = email;
       this.credito = credito;
       
       
       
   }

    public String getNome() {
        return nome;
    }

    

    public float getCredito() {
        return this.credito;
    }

    public void setCredito(float credito) {
        this.credito = credito;
    }

    @Override
    public String toString() {
        return "cliente{" + "nome=" + nome + ", email=" + email + ", credito=" + credito + '}';
    }
    public boolean fazerCompra(float valor){
        if(valor> credito){
            return false;
        }
        else{
            credito -= valor;
                    return true;
        }
    }
    public void quitarDivida(float valor){
        credito += valor;
    }
}
