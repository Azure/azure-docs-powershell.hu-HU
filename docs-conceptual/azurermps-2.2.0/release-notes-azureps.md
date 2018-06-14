---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854613"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

## <a name="version-220"></a>2.2.0-ás verzió
* Compute
  - A titkosítás állapotának az AzureDiskEncryptionForLinux bővítményből történő lekérésének támogatása
* DataFactory
  - Új parancsmag hozzáadása a tevékenységablakok felsorolásához
    + Get-AzureRmDataFactoryActivityWindow
* DataLake
  - A `Host` paraméter lecserélése a `DatabaseHost` paraméterre, valamint alias hozzáadása a `Host` paraméterhez.
    + New-AzureRmDataLakeAnalyticsCatalogSecret
    + Set-AzureRmDataLakeAnalyticsCatalogSecret
  - Az ACL és alapértelmezett ACL eltávolításának támogatása
  - Névtelen engedélyek beszerzésének és beállításának támogatása fájlok és mappák esetében
* KeyVault
  - Tanúsítványok támogatása
    + Add-AzureKeyVaultCertificate
    + Add-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificate
    + Get-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificateIssuer
    + Get-AzureKeyVaultCertificateOperation
    + Get-AzureKeyVaultCertificatePolicy
    + Import-AzureKeyVaultCertificate
    + New-AzureKeyVaultCertificateAdministratorDetails
    + New-AzureKeyVaultCertificateOrganizationDetails
    + New-AzureKeyVaultCertificatePolicy
    + Remove-AzureKeyVaultCertificate
    + Remove-AzureKeyVaultCertificateContact
    + Remove-AzureKeyVaultCertificateIssuer
    + Remove-AzureKeyVaultCertificateOperation
    + Set-AzureKeyVaultCertificateAttribute
    + Set-AzureKeyVaultCertificateIssuer
    + Set-AzureKeyVaultCertificatePolicy
    + Stop-AzureKeyVaultCertificateOperation
* Network (Hálózat)

  - Új kapcsolóparaméter hozzáadása a hálózati adapter számára a gyorsított hálózatkezelés engedélyezéséhez/letiltásához – +New-AzureRmNetworkInterface -EnableAcceleratedNetworking
  - Aktív-aktív átjárószolgáltatás PowerShell-parancsmagjainak engedélyezése
    + Add-AzureRmVirtualNetworkGatewayIpConfig
    + Remove-AzureRmVirtualNetworkGatewayIpConfig
  - Új parancsmag hozzáadása
    + Test-AzureRmPrivateIpAddressAvailability
* További források
  - Zónák támogatása szolgáltatói és erőforrás-parancsmagok esetében
    + Get-AzureRmProvider
    + New-AzureRmResource
    + Set-AzureRmResource
* SQL
  - Új parancsmagok hozzáadása az Azure SQL fenyegetésészlelési házirendkezelése számára a kiszolgálók szintjén
    + Get-AzureRmSqlServerThreatDetectionPolicy
    + Remove-AzureRmSqlServerThreatDetectionPolicy
    + Set-AzureRmSqlServerThreatDetectionPolicy
  - Új parancsmagok hozzáadása a GeoBackupPolicy paraméter engedélyezésének/letiltásának támogatása érdekében az SQL Azure-adattárházak esetében
    + Get-AzureRmSqlDatabaseGeoBackupPolicy
    + Set-AzureRmSqlDatabaseGeoBackupPolicy
  - Új parancsmagok hozzáadása az Azure SQL-tanácsadók és Javasolt műveletek API-k számára
    + Get-AzureRmSqlDatabaseAdvisor
    + Get-AzureRmSqlElasticPoolAdvisor
    + Get-AzureRmSqlServerAdvisor
    + Get-AzureRmSqlDatabaseRecommendedActions
    + Get-AzureRmSqlElasticPoolRecommendedActions
    + Get-AzureRmSqlServerRecommendedActions
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus
    + Set-AzureRmSqlDatabaseRecommendedActionState
    + Set-AzureRmSqlElasticPoolRecommendedActionState
    + Set-AzureRmSqlServerRecommendedActionState
