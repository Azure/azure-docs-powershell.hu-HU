---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669751"
---
# <span data-ttu-id="9b5d2-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="9b5d2-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="9b5d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5d2-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy automatikusan védjék az összes meglévő védtelen DBs-t és egy olyan DB-t, amelyet később felvesznek a megadott házirenddel.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="9b5d2-104">Az Azure Backup szolgáltatás ezután rendszeresen ellenőrzi az automatikusan védett tárolókat az új DBs-ben, és automatikusan megvédi őket.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="9b5d2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b5d2-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5d2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b5d2-106">DESCRIPTION</span></span>
<span data-ttu-id="9b5d2-107">Az **enable-AzRecoveryServicesBackupAutoProtection** parancsmag az Azure Auto Backup Protection házirendjét egy védett elemen állítja be.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="9b5d2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9b5d2-108">EXAMPLES</span></span>

### <span data-ttu-id="9b5d2-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b5d2-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="9b5d2-110">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="9b5d2-111">A második parancsmag a $Pol házirendjét használva állítja be a AzureWorkload a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="9b5d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b5d2-112">PARAMETERS</span></span>

### <span data-ttu-id="9b5d2-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9b5d2-113">-BackupManagementType</span></span>
<span data-ttu-id="9b5d2-114">Az erőforrás biztonságimásolat-kezelési típusa (például: Mohácsi, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="9b5d2-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5d2-115">-DefaultProfile</span></span>
<span data-ttu-id="9b5d2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5d2-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="9b5d2-117">-InputItem</span></span>
<span data-ttu-id="9b5d2-118">Annak a védett elemnek az objektumát adja meg, amely bemenetként továbbítható.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-118">Specifies the protectable item object that can be passed as an input.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5d2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b5d2-119">-PassThru</span></span>
<span data-ttu-id="9b5d2-120">Az automatikus védelem eredményének visszaadása.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="9b5d2-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="9b5d2-121">-Policy</span></span>
<span data-ttu-id="9b5d2-122">Protection Policy objektum.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5d2-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9b5d2-123">-VaultId</span></span>
<span data-ttu-id="9b5d2-124">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="9b5d2-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9b5d2-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="9b5d2-125">-WorkloadType</span></span>
<span data-ttu-id="9b5d2-126">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="9b5d2-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5d2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b5d2-127">-Confirm</span></span>
<span data-ttu-id="9b5d2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5d2-129">-WhatIf</span></span>
<span data-ttu-id="9b5d2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b5d2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b5d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5d2-132">CommonParameters</span></span>
<span data-ttu-id="9b5d2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b5d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5d2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5d2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5d2-135">INPUTS</span></span>

### <span data-ttu-id="9b5d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5d2-136">System.String</span></span>

## <span data-ttu-id="9b5d2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5d2-137">OUTPUTS</span></span>

### <span data-ttu-id="9b5d2-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9b5d2-138">System.Object</span></span>

## <span data-ttu-id="9b5d2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b5d2-139">NOTES</span></span>

## <span data-ttu-id="9b5d2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b5d2-140">RELATED LINKS</span></span>