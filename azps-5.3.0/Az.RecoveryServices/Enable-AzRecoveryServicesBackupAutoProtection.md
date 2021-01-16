---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476777"
---
# <span data-ttu-id="176f7-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="176f7-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="176f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176f7-102">SYNOPSIS</span></span>
<span data-ttu-id="176f7-103">Az **Enable-AzRecoveryServicesBackupAutoProtection** parancsmag a megadott házirendnek megfelelő aktuális és jövőbeli SQL-DBs automatikus védelmét állítja be a megadott példányon belül.</span><span class="sxs-lookup"><span data-stu-id="176f7-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="176f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="176f7-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="176f7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="176f7-105">DESCRIPTION</span></span>
<span data-ttu-id="176f7-106">Ez a parancs lehetővé teszi a felhasználóknak, hogy automatikusan védjék az összes meglévő nem védett SQL-DBs-t és minden olyan adatbázis-adatbázist, amelyet később hozzáad a megadott házirendhez.</span><span class="sxs-lookup"><span data-stu-id="176f7-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="176f7-107">Mivel az utasítás az összes jövőbeli DBs biztonsági mentése, a művelet SQLInstance szinten történik, az Azure biztonsági mentési szolgáltatás ezután rendszeresen ellenőrzi az automatikusan védett tárolókat az új DB-k után, és automatikusan védi őket.</span><span class="sxs-lookup"><span data-stu-id="176f7-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="176f7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="176f7-108">EXAMPLES</span></span>

### <span data-ttu-id="176f7-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="176f7-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="176f7-110">Az első parancsmag kap egy alapértelmezett házirendobjektumot, majd tárolja azt a $Pol változóban.</span><span class="sxs-lookup"><span data-stu-id="176f7-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="176f7-111">A második parancsmag lekéri a megfelelő SQLInstance függvényt, amely egy védett elem.</span><span class="sxs-lookup"><span data-stu-id="176f7-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="176f7-112">A 3. parancs ezután beállítja az automatikus védelmet ehhez a példányhoz a $Pol.</span><span class="sxs-lookup"><span data-stu-id="176f7-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="176f7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="176f7-113">Example 2</span></span>

<span data-ttu-id="176f7-114">Ez a parancs lehetővé teszi a felhasználóknak, hogy automatikusan védjék az összes meglévő nem védett DBs-t és minden olyan adatbázis-adatbázist, amelyet később hozzáadnak az adott házirendhez.</span><span class="sxs-lookup"><span data-stu-id="176f7-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="176f7-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="176f7-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="176f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176f7-116">PARAMETERS</span></span>

### <span data-ttu-id="176f7-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="176f7-117">-BackupManagementType</span></span>
<span data-ttu-id="176f7-118">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="176f7-118">The class of resources being protected.</span></span> <span data-ttu-id="176f7-119">Az ehhez a parancsmaghoz jelenleg a KÖVETKEZŐ értékek támogatottak: MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="176f7-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="176f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176f7-120">-DefaultProfile</span></span>
<span data-ttu-id="176f7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="176f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176f7-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="176f7-122">-InputItem</span></span>
<span data-ttu-id="176f7-123">Megadja azt a védett elemobjektumot, amely bemenetként adható át.</span><span class="sxs-lookup"><span data-stu-id="176f7-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="176f7-124">A jelenlegi támogatott érték egy "SQLInstance" típusú védhetőItem objektum.</span><span class="sxs-lookup"><span data-stu-id="176f7-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="176f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="176f7-125">-PassThru</span></span>
<span data-ttu-id="176f7-126">Adja vissza az eredményt az automatikus védelem érdekében.</span><span class="sxs-lookup"><span data-stu-id="176f7-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="176f7-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="176f7-127">-Policy</span></span>
<span data-ttu-id="176f7-128">Védelmi házirend objektum.</span><span class="sxs-lookup"><span data-stu-id="176f7-128">Protection policy object.</span></span>

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

### <span data-ttu-id="176f7-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="176f7-129">-VaultId</span></span>
<span data-ttu-id="176f7-130">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="176f7-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="176f7-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="176f7-131">-WorkloadType</span></span>
<span data-ttu-id="176f7-132">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="176f7-132">Workload type of the resource.</span></span> <span data-ttu-id="176f7-133">A támogatott értékek jelenleg az AzureVM, a WindowsServer, az MSSQL</span><span class="sxs-lookup"><span data-stu-id="176f7-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="176f7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176f7-134">-Confirm</span></span>
<span data-ttu-id="176f7-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="176f7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176f7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176f7-136">-WhatIf</span></span>
<span data-ttu-id="176f7-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="176f7-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="176f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176f7-138">CommonParameters</span></span>
<span data-ttu-id="176f7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176f7-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="176f7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176f7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="176f7-141">INPUTS</span></span>

### <span data-ttu-id="176f7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="176f7-142">System.String</span></span>

## <span data-ttu-id="176f7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="176f7-143">OUTPUTS</span></span>

### <span data-ttu-id="176f7-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="176f7-144">System.Object</span></span>

## <span data-ttu-id="176f7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="176f7-145">NOTES</span></span>

## <span data-ttu-id="176f7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="176f7-146">RELATED LINKS</span></span>
