---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672907"
---
# <span data-ttu-id="dd14a-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="dd14a-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="dd14a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd14a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd14a-103">A SCDPM-kiszolgáló vagy a biztonsági másolat kiszolgálójának törlése a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="dd14a-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd14a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd14a-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd14a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd14a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd14a-106">A **unregister-AzureRmRecoveryServicesBackupManagementServer** parancsmag a System Center Data Protection Manager (SCDPM) kiszolgálóját vagy az Azure Backup Servert a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="dd14a-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="dd14a-107">Ez a parancsmag eltávolítja azokat a kiszolgálókat, amelyek nem lettek rögzítve a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="dd14a-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="dd14a-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="dd14a-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="dd14a-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="dd14a-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="dd14a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dd14a-110">EXAMPLES</span></span>

### <span data-ttu-id="dd14a-111">1. példa: SCDPM-kiszolgáló regisztrációjának megszüntetése a boltozatról</span><span class="sxs-lookup"><span data-stu-id="dd14a-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="dd14a-112">Az első parancs a dpmserver01.contoso.com nevű Backup Management Servert kapja, majd a $BMS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd14a-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="dd14a-113">A második parancs a SCDPM-kiszolgáló regisztrációját a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="dd14a-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="dd14a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd14a-114">PARAMETERS</span></span>

### <span data-ttu-id="dd14a-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="dd14a-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="dd14a-116">Itt adhatja meg a SCDPM-kiszolgáló objektumát a regisztráció törléséhez.</span><span class="sxs-lookup"><span data-stu-id="dd14a-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="dd14a-117">**BackupManagementServer** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupManagementServer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dd14a-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd14a-118">-DefaultProfile</span></span>
<span data-ttu-id="dd14a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd14a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd14a-120">-PassThru</span></span>
<span data-ttu-id="dd14a-121">Adja vissza a törölni kívánt biztonságimásolat-kezelési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="dd14a-121">Return the Backup Management Server to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dd14a-122">-VaultId</span></span>
<span data-ttu-id="dd14a-123">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="dd14a-123">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd14a-124">-Confirm</span></span>
<span data-ttu-id="dd14a-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd14a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd14a-126">-WhatIf</span></span>
<span data-ttu-id="dd14a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd14a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd14a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd14a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd14a-129">CommonParameters</span></span>
<span data-ttu-id="dd14a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd14a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd14a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd14a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd14a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd14a-132">INPUTS</span></span>

### <span data-ttu-id="dd14a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd14a-133">System.String</span></span>
<span data-ttu-id="dd14a-134">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd14a-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="dd14a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd14a-135">OUTPUTS</span></span>

### <span data-ttu-id="dd14a-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="dd14a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="dd14a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd14a-137">NOTES</span></span>

## <span data-ttu-id="dd14a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd14a-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd14a-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="dd14a-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


