---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160203"
---
# <span data-ttu-id="a6b79-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a6b79-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="a6b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6b79-102">SYNOPSIS</span></span>

<span data-ttu-id="a6b79-103">Egy biztonságiolt elem helyreállítási pontjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a6b79-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="a6b79-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6b79-104">SYNTAX</span></span>

### <span data-ttu-id="a6b79-105">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6b79-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6b79-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="a6b79-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6b79-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="a6b79-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6b79-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6b79-108">DESCRIPTION</span></span>

<span data-ttu-id="a6b79-109">A **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmag leküldi a biztonsági másolatként használt Azure Biztonsági másolat elem helyreállítási pontjait.</span><span class="sxs-lookup"><span data-stu-id="a6b79-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="a6b79-110">Miután biztonságiolt egy elemet, egy **AzureRmRecoveryServicesBackupRecoveryPoint-objektum** egy vagy több helyreállítási ponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="a6b79-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="a6b79-111">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="a6b79-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="a6b79-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6b79-112">EXAMPLES</span></span>

### <span data-ttu-id="a6b79-113">1. példa: Helyreállítási pontok lekérte az elem előző hetének helyreállítási pontjait</span><span class="sxs-lookup"><span data-stu-id="a6b79-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="a6b79-114">Az első parancs a vault-objektumot a vaultName alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a6b79-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="a6b79-115">A második parancs hét nappal ezelőtti dátumot ad vissza, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="a6b79-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a6b79-116">A harmadik parancs megkapja a mai dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="a6b79-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a6b79-117">A negyedik parancs lekérte az AzureVM biztonsági mentési tárolóit, és tárolja őket a $Container változóban.</span><span class="sxs-lookup"><span data-stu-id="a6b79-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="a6b79-118">Az ötödik parancs lekérte a biztonságimásolat-elemet a workloadType( tárolóazonosító) alapján, majd tárolja azt a $BackupItem változóban.</span><span class="sxs-lookup"><span data-stu-id="a6b79-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a6b79-119">Az utolsó parancs egy tömb helyreállítási pontot kap az elemhez a $BackupItem, majd tárolja őket a $RP változóban.</span><span class="sxs-lookup"><span data-stu-id="a6b79-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="a6b79-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6b79-120">PARAMETERS</span></span>

### <span data-ttu-id="a6b79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b79-121">-DefaultProfile</span></span>

<span data-ttu-id="a6b79-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6b79-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b79-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a6b79-123">-EndDate</span></span>

<span data-ttu-id="a6b79-124">A dátumtartomány végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6b79-124">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b79-125">-Item</span><span class="sxs-lookup"><span data-stu-id="a6b79-125">-Item</span></span>

<span data-ttu-id="a6b79-126">Azt az elemet adja meg, amelyhez a parancsmag helyreállítási pontokat kap.</span><span class="sxs-lookup"><span data-stu-id="a6b79-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="a6b79-127">**AzureRmRecoveryServicesBackupItem** objektum beszerzéséhez használja a **Get-AzRecoveryServicesBackupItem** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a6b79-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b79-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="a6b79-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="a6b79-129">Megadja a titkosított virtuális gép KeyVault-kulcsának visszaállításához szükséges bemeneti fájl letöltési helyét.</span><span class="sxs-lookup"><span data-stu-id="a6b79-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b79-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="a6b79-130">-RecoveryPointId</span></span>

<span data-ttu-id="a6b79-131">A helyreállításipont-azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6b79-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b79-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a6b79-132">-StartDate</span></span>

<span data-ttu-id="a6b79-133">A dátumtartomány kezdő időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6b79-133">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b79-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a6b79-134">-VaultId</span></span>

<span data-ttu-id="a6b79-135">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a6b79-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a6b79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b79-136">CommonParameters</span></span>
<span data-ttu-id="a6b79-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b79-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6b79-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b79-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6b79-139">INPUTS</span></span>

### <span data-ttu-id="a6b79-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="a6b79-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="a6b79-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a6b79-141">System.String</span></span>

## <span data-ttu-id="a6b79-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6b79-142">OUTPUTS</span></span>

### <span data-ttu-id="a6b79-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a6b79-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a6b79-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6b79-144">NOTES</span></span>

## <span data-ttu-id="a6b79-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6b79-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6b79-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a6b79-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a6b79-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a6b79-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
