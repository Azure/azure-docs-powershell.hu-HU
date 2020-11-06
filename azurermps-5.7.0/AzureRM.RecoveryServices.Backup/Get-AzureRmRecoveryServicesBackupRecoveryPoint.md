---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493067"
---
# <span data-ttu-id="02759-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="02759-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="02759-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02759-102">SYNOPSIS</span></span>
<span data-ttu-id="02759-103">A mentett elem helyreállítási pontjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02759-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02759-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02759-104">SYNTAX</span></span>

### <span data-ttu-id="02759-105">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02759-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02759-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="02759-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02759-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="02759-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02759-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02759-108">DESCRIPTION</span></span>
<span data-ttu-id="02759-109">A **Get-AzureRmRecoveryServicesBackupRecoveryPoint** parancsmag helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatához.</span><span class="sxs-lookup"><span data-stu-id="02759-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="02759-110">Miután biztonsági másolatot készített egy elemről, egy **AzureRmRecoveryServicesBackupRecoveryPoint** -objektumnak egy vagy több helyreállítási pontja van.</span><span class="sxs-lookup"><span data-stu-id="02759-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="02759-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="02759-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="02759-112">Példák</span><span class="sxs-lookup"><span data-stu-id="02759-112">EXAMPLES</span></span>

### <span data-ttu-id="02759-113">Példa 1: helyreállítási pontok beszerzése az adott elem utolsó hetében</span><span class="sxs-lookup"><span data-stu-id="02759-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="02759-114">Az első parancs hét nappal ezelőtt kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02759-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="02759-115">A második parancs a mai dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02759-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="02759-116">A harmadik parancs AzureVM kapja a biztonsági másolat tárolóját, és a $Containers változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="02759-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="02759-117">A negyedik parancs a V2VM nevű biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02759-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="02759-118">Az utolsó parancs a $BackupItemben található elem helyreállítási pontjának tömbjét kapja, majd a $RP változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="02759-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="02759-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02759-119">PARAMETERS</span></span>

### <span data-ttu-id="02759-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02759-120">-DefaultProfile</span></span>
<span data-ttu-id="02759-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02759-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02759-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="02759-122">-EndDate</span></span>
<span data-ttu-id="02759-123">A dátumtartomány végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02759-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02759-124">-Elem</span><span class="sxs-lookup"><span data-stu-id="02759-124">-Item</span></span>
<span data-ttu-id="02759-125">Annak az elemnek a meghatározása, amelyre a parancsmag helyreállítási pontokat kap.</span><span class="sxs-lookup"><span data-stu-id="02759-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="02759-126">**AzureRmRecoveryServicesBackupItem** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02759-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02759-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="02759-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="02759-128">Annak a helynek a helye, ahol a bemeneti fájl letöltésével visszaállíthatja egy titkosított virtuális gép kulcskezelő kulcsát.</span><span class="sxs-lookup"><span data-stu-id="02759-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02759-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="02759-129">-RecoveryPointId</span></span>
<span data-ttu-id="02759-130">A helyreállítási pont AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02759-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02759-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="02759-131">-StartDate</span></span>
<span data-ttu-id="02759-132">A dátumtartomány kezdetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02759-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02759-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02759-133">CommonParameters</span></span>
<span data-ttu-id="02759-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02759-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02759-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02759-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02759-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02759-136">INPUTS</span></span>

### <span data-ttu-id="02759-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="02759-137">ItemBase</span></span>
<span data-ttu-id="02759-138">A "tétel" paraméter értéke az "ItemBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="02759-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="02759-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02759-139">OUTPUTS</span></span>

### <span data-ttu-id="02759-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="02759-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="02759-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="02759-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="02759-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02759-142">NOTES</span></span>

## <span data-ttu-id="02759-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02759-143">RELATED LINKS</span></span>

[<span data-ttu-id="02759-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="02759-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="02759-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="02759-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


