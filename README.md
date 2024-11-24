# Proyecto de NFT en Arbitrum Sepolia y Sepolia

> Implementación de un NFT básico utilizando **Scaffold ETH** y adaptado para operar en las redes **Arbitrum Sepolia** y **Sepolia**. 

---

## Contratos desplegados

### 🌟 Contrato en Arbitrum Sepolia
El contrato fue desplegado exitosamente en la red **Arbitrum Sepolia**. Consulta los detalles aquí:

🔗 [Transacción en Arbitrum Sepolia](https://sepolia.arbiscan.io/tx/0x4093dd8f1439451b21d60507a3c64e79380dc80b6345c5fc1a8f27902249fa45)

### 🌟 Contratos en Sepolia
Se desplegaron los siguientes contratos en la red **Sepolia**:

🔗 [Transacción en Sepolia - Contrato 1](https://sepolia.etherscan.io/tx/0xdd2832caf1ab80c942b31a114420d62ae262a784849fad7ee8f4f2f79c580537)
🔗 [Transacción en Sepolia - Contrato 2](https://sepolia.etherscan.io/tx/0xcd3669b9f38cdc8e8f481c21dffcc4fed81edcfd0e5f5156908dcb9eabe1f973)

---

## OpenSea

### Visualización de NFTs en OpenSea:
- **Arbitrum Sepolia:**  
  [NFT en OpenSea - Arbitrum Sepolia](https://testnets.opensea.io/es/assets/arbitrum-sepolia/0x5eae29b5fb863b1633ac42a35945c45d3bd83a07/7)

- **Sepolia:**  
  [NFT en OpenSea - Sepolia](https://testnets.opensea.io/es/assets/sepolia/0x20f7090ca832e45352dd6ad0d877bc0abc6e0cbc/2)

---

## Solución al Error de CORS y Configuración de Alchemy

Durante el desarrollo, surgió un error de CORS debido a que en mi caso me conectaba a un RPC público de Sepolia (rpc.sepolia.org), que tiene restricciones y no permite conexiones directas desde localhost. Para resolver esto, se migra a un proveedor profesional, Alchemy, que ofrece una línea RPC privada y dedicada.

Los RPC públicos como el de Sepolia son gratuitos, pero tienen limitaciones (como el error de CORS desde localhost). Usar un RPC profesional como el de Alchemy garantiza estabilidad y accesibilidad sin restricciones.

```mermaid
graph TD
    A[Desarrollo Local] --> B[Usa .env.local]
    C[Producción/Vercel] --> D[Usa Variables de Entorno de Vercel]
    E[Git Repository] --> F[No contiene .env.local]
