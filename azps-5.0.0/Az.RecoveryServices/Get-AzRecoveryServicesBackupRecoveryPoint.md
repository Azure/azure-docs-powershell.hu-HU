---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187922"
---
# <span data-ttu-id="89ff5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="89ff5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="89ff5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89ff5-102">SYNOPSIS</span></span>

<span data-ttu-id="89ff5-103">A mentett elem helyreállítási pontjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="89ff5-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="89ff5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89ff5-104">SYNTAX</span></span>

### <span data-ttu-id="89ff5-105">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89ff5-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ff5-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="89ff5-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ff5-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="89ff5-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89ff5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="89ff5-108">DESCRIPTION</span></span>

<span data-ttu-id="89ff5-109">A **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmag helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatához.</span><span class="sxs-lookup"><span data-stu-id="89ff5-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="89ff5-110">Miután biztonsági másolatot készített egy elemről, egy **AzureRmRecoveryServicesBackupRecoveryPoint** -objektumnak egy vagy több helyreállítási pontja van.</span><span class="sxs-lookup"><span data-stu-id="89ff5-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="89ff5-111">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="89ff5-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="89ff5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="89ff5-112">EXAMPLES</span></span>

### <span data-ttu-id="89ff5-113">Példa 1: helyreállítási pontok beszerzése az adott elem utolsó hetében</span><span class="sxs-lookup"><span data-stu-id="89ff5-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="89ff5-114">Az első parancs a vaultName alapján kapja meg a boltozat objektumát.</span><span class="sxs-lookup"><span data-stu-id="89ff5-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="89ff5-115">A második parancs hét nappal ezelőtt kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89ff5-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="89ff5-116">A harmadik parancs a mai dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89ff5-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="89ff5-117">A negyedik parancs AzureVM-tároló tárolókat kap, és a $Container változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="89ff5-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="89ff5-118">Az ötödik parancs a biztonsági másolatot a workloadType, az vaultId és a a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89ff5-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="89ff5-119">Az utolsó parancs a $BackupItemben található elem helyreállítási pontjának tömbjét kapja, majd a $RP változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="89ff5-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="89ff5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89ff5-120">PARAMETERS</span></span>

### <span data-ttu-id="89ff5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ff5-121">-DefaultProfile</span></span>

<span data-ttu-id="89ff5-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89ff5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89ff5-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="89ff5-123">-EndDate</span></span>

<span data-ttu-id="89ff5-124">A dátumtartomány végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89ff5-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="89ff5-125">-Elem</span><span class="sxs-lookup"><span data-stu-id="89ff5-125">-Item</span></span>

<span data-ttu-id="89ff5-126">Annak az elemnek a meghatározása, amelyre a parancsmag helyreállítási pontokat kap.</span><span class="sxs-lookup"><span data-stu-id="89ff5-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="89ff5-127">Ha **AzureRmRecoveryServicesBackupItem** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupItem** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89ff5-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="89ff5-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="89ff5-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="89ff5-129">Annak a helynek a helye, ahol a bemeneti fájl letöltésével visszaállíthatja egy titkosított virtuális gép kulcskezelő kulcsát.</span><span class="sxs-lookup"><span data-stu-id="89ff5-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="89ff5-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="89ff5-130">-RecoveryPointId</span></span>

<span data-ttu-id="89ff5-131">A helyreállítási pont AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="89ff5-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="89ff5-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="89ff5-132">-StartDate</span></span>

<span data-ttu-id="89ff5-133">A dátumtartomány kezdetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89ff5-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="89ff5-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="89ff5-134">-VaultId</span></span>

<span data-ttu-id="89ff5-135">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="89ff5-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="89ff5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ff5-136">CommonParameters</span></span>
<span data-ttu-id="89ff5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89ff5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ff5-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89ff5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ff5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ff5-139">INPUTS</span></span>

### <span data-ttu-id="89ff5-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="89ff5-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="89ff5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89ff5-141">System.String</span></span>

## <span data-ttu-id="89ff5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ff5-142">OUTPUTS</span></span>

### <span data-ttu-id="89ff5-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="89ff5-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="89ff5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89ff5-144">NOTES</span></span>

## <span data-ttu-id="89ff5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89ff5-145">RELATED LINKS</span></span>

[<span data-ttu-id="89ff5-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="89ff5-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="89ff5-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89ff5-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
