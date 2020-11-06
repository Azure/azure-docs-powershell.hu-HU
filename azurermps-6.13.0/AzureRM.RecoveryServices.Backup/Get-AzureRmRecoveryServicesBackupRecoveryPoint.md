---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498200"
---
# <span data-ttu-id="30225-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="30225-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="30225-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30225-102">SYNOPSIS</span></span>
<span data-ttu-id="30225-103">A mentett elem helyreállítási pontjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="30225-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30225-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30225-104">SYNTAX</span></span>

### <span data-ttu-id="30225-105">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30225-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30225-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="30225-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30225-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="30225-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30225-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="30225-108">DESCRIPTION</span></span>
<span data-ttu-id="30225-109">A **Get-AzureRmRecoveryServicesBackupRecoveryPoint** parancsmag helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatához.</span><span class="sxs-lookup"><span data-stu-id="30225-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="30225-110">Miután biztonsági másolatot készített egy elemről, egy **AzureRmRecoveryServicesBackupRecoveryPoint** -objektumnak egy vagy több helyreállítási pontja van.</span><span class="sxs-lookup"><span data-stu-id="30225-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="30225-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="30225-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="30225-112">Példák</span><span class="sxs-lookup"><span data-stu-id="30225-112">EXAMPLES</span></span>

### <span data-ttu-id="30225-113">Példa 1: helyreállítási pontok beszerzése az adott elem utolsó hetében</span><span class="sxs-lookup"><span data-stu-id="30225-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="30225-114">Az első parancs hét nappal ezelőtt kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="30225-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="30225-115">A második parancs a mai dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="30225-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="30225-116">A harmadik parancs AzureVM kapja a biztonsági másolat tárolóját, és a $Containers változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="30225-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="30225-117">A negyedik parancs a V2VM nevű biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="30225-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="30225-118">Az utolsó parancs a $BackupItemben található elem helyreállítási pontjának tömbjét kapja, majd a $RP változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="30225-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="30225-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30225-119">PARAMETERS</span></span>

### <span data-ttu-id="30225-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30225-120">-DefaultProfile</span></span>
<span data-ttu-id="30225-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30225-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30225-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="30225-122">-EndDate</span></span>
<span data-ttu-id="30225-123">A dátumtartomány végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30225-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="30225-124">-Elem</span><span class="sxs-lookup"><span data-stu-id="30225-124">-Item</span></span>
<span data-ttu-id="30225-125">Annak az elemnek a meghatározása, amelyre a parancsmag helyreállítási pontokat kap.</span><span class="sxs-lookup"><span data-stu-id="30225-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="30225-126">**AzureRmRecoveryServicesBackupItem** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30225-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="30225-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="30225-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="30225-128">Annak a helynek a helye, ahol a bemeneti fájl letöltésével visszaállíthatja egy titkosított virtuális gép kulcskezelő kulcsát.</span><span class="sxs-lookup"><span data-stu-id="30225-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="30225-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="30225-129">-RecoveryPointId</span></span>
<span data-ttu-id="30225-130">A helyreállítási pont AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="30225-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="30225-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="30225-131">-StartDate</span></span>
<span data-ttu-id="30225-132">A dátumtartomány kezdetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30225-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="30225-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="30225-133">-VaultId</span></span>
<span data-ttu-id="30225-134">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="30225-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="30225-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30225-135">CommonParameters</span></span>
<span data-ttu-id="30225-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30225-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30225-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30225-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30225-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30225-138">INPUTS</span></span>

### <span data-ttu-id="30225-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="30225-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="30225-140">Paraméterek: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30225-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="30225-141">System. String</span><span class="sxs-lookup"><span data-stu-id="30225-141">System.String</span></span>
<span data-ttu-id="30225-142">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30225-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="30225-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30225-143">OUTPUTS</span></span>

### <span data-ttu-id="30225-144">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="30225-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="30225-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30225-145">NOTES</span></span>

## <span data-ttu-id="30225-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30225-146">RELATED LINKS</span></span>

[<span data-ttu-id="30225-147">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="30225-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="30225-148">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="30225-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


