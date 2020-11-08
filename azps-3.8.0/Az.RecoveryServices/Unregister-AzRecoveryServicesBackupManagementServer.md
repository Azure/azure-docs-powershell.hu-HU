---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 8d0ecda3c93ac20205cac0ea8bc406a218065a81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011605"
---
# <span data-ttu-id="081b3-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="081b3-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="081b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="081b3-102">SYNOPSIS</span></span>
<span data-ttu-id="081b3-103">A SCDPM-kiszolgáló vagy a biztonsági másolat kiszolgálójának törlése a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="081b3-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="081b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="081b3-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="081b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="081b3-105">DESCRIPTION</span></span>
<span data-ttu-id="081b3-106">A **unregister-AzRecoveryServicesBackupManagementServer** parancsmag a System Center Data Protection Manager (SCDPM) kiszolgálóját vagy az Azure Backup Servert a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="081b3-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="081b3-107">Ez a parancsmag eltávolítja azokat a kiszolgálókat, amelyek nem lettek rögzítve a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="081b3-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="081b3-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="081b3-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="081b3-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="081b3-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="081b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="081b3-110">EXAMPLES</span></span>

### <span data-ttu-id="081b3-111">1. példa: SCDPM-kiszolgáló regisztrációjának megszüntetése a boltozatról</span><span class="sxs-lookup"><span data-stu-id="081b3-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="081b3-112">Az első parancs a dpmserver01.contoso.com nevű Backup Management Servert kapja, majd a $BMS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="081b3-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="081b3-113">A második parancs a SCDPM-kiszolgáló regisztrációját a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="081b3-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="081b3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="081b3-114">PARAMETERS</span></span>

### <span data-ttu-id="081b3-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="081b3-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="081b3-116">A helyreállítási szolgáltatások biztonságimásolat-tárolója.</span><span class="sxs-lookup"><span data-stu-id="081b3-116">The recovery services backup container.</span></span>

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

### <span data-ttu-id="081b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081b3-117">-DefaultProfile</span></span>
<span data-ttu-id="081b3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="081b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081b3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="081b3-119">-PassThru</span></span>
<span data-ttu-id="081b3-120">Adja vissza a törölni kívánt biztonságimásolat-kezelési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="081b3-120">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="081b3-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="081b3-121">-VaultId</span></span>
<span data-ttu-id="081b3-122">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="081b3-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="081b3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="081b3-123">-Confirm</span></span>
<span data-ttu-id="081b3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="081b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="081b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081b3-125">-WhatIf</span></span>
<span data-ttu-id="081b3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="081b3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="081b3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="081b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="081b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081b3-128">CommonParameters</span></span>
<span data-ttu-id="081b3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="081b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081b3-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="081b3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081b3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="081b3-131">INPUTS</span></span>

### <span data-ttu-id="081b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="081b3-132">System.String</span></span>

## <span data-ttu-id="081b3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="081b3-133">OUTPUTS</span></span>

### <span data-ttu-id="081b3-134">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="081b3-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="081b3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="081b3-135">NOTES</span></span>

## <span data-ttu-id="081b3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="081b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="081b3-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="081b3-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


