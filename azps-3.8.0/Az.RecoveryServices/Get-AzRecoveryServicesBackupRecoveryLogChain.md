---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014733"
---
# <span data-ttu-id="22b16-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="22b16-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="22b16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22b16-102">SYNOPSIS</span></span>
<span data-ttu-id="22b16-103">Ez a parancs felsorolja a biztonsági másolatban szereplő töretlen log-elem kezdési és befejezési pontját.</span><span class="sxs-lookup"><span data-stu-id="22b16-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="22b16-104">Annak megállapításához, hogy az a pont, amelyen a felhasználó vissza kívánja állítani, érvényes-e vagy nem.</span><span class="sxs-lookup"><span data-stu-id="22b16-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="22b16-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22b16-105">SYNTAX</span></span>

### <span data-ttu-id="22b16-106">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22b16-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22b16-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="22b16-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b16-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="22b16-108">DESCRIPTION</span></span>
<span data-ttu-id="22b16-109">A **Get-AzRecoveryServicesBackupRecoveryLogChain** parancsmag időtartomány-helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="22b16-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="22b16-110">Egy elem biztonsági mentése után egy **AzRecoveryServicesBackupRecoveryLogChain** -objektumnak egy vagy több helyreállítási időtartománya van.</span><span class="sxs-lookup"><span data-stu-id="22b16-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="22b16-111">Példák</span><span class="sxs-lookup"><span data-stu-id="22b16-111">EXAMPLES</span></span>

### <span data-ttu-id="22b16-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22b16-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="22b16-113">Az első parancs hét nappal ezelőtt kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22b16-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="22b16-114">A második parancs a mai dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22b16-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="22b16-115">A harmadik parancs AzureWorkload kapja a biztonsági másolat tárolóját, és a $Containers változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="22b16-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="22b16-116">A negyedik parancs a biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22b16-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="22b16-117">Az utolsó parancs a $BackupItemben található elem helyreállítási pontjának időtartományai sorát kapja, majd a $RP változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="22b16-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="22b16-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22b16-118">PARAMETERS</span></span>

### <span data-ttu-id="22b16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b16-119">-DefaultProfile</span></span>
<span data-ttu-id="22b16-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22b16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b16-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="22b16-121">-EndDate</span></span>
<span data-ttu-id="22b16-122">Annak a időtartománynak a záró időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="22b16-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="22b16-123">-Elem</span><span class="sxs-lookup"><span data-stu-id="22b16-123">-Item</span></span>
<span data-ttu-id="22b16-124">Védett elem objektum, amelynek helyreállítási pontját le kell olvasni</span><span class="sxs-lookup"><span data-stu-id="22b16-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="22b16-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="22b16-125">-StartDate</span></span>
<span data-ttu-id="22b16-126">Az időtartomány kezdési időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="22b16-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="22b16-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="22b16-127">-VaultId</span></span>
<span data-ttu-id="22b16-128">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="22b16-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="22b16-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b16-129">CommonParameters</span></span>
<span data-ttu-id="22b16-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22b16-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b16-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22b16-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b16-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b16-132">INPUTS</span></span>

### <span data-ttu-id="22b16-133">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="22b16-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="22b16-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22b16-134">System.String</span></span>

## <span data-ttu-id="22b16-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b16-135">OUTPUTS</span></span>

### <span data-ttu-id="22b16-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="22b16-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="22b16-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22b16-137">NOTES</span></span>

## <span data-ttu-id="22b16-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22b16-138">RELATED LINKS</span></span>
