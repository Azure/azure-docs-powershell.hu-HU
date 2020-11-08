---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184700"
---
# <span data-ttu-id="2c587-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2c587-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2c587-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c587-102">SYNOPSIS</span></span>
<span data-ttu-id="2c587-103">Ez a parancs felsorolja a biztonsági másolatban szereplő töretlen log-elem kezdési és befejezési pontját.</span><span class="sxs-lookup"><span data-stu-id="2c587-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2c587-104">Annak megállapításához, hogy az a pont, amelyen a felhasználó vissza kívánja állítani, érvényes-e vagy nem.</span><span class="sxs-lookup"><span data-stu-id="2c587-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2c587-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c587-105">SYNTAX</span></span>

### <span data-ttu-id="2c587-106">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c587-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c587-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2c587-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c587-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c587-108">DESCRIPTION</span></span>
<span data-ttu-id="2c587-109">A **Get-AzRecoveryServicesBackupRecoveryLogChain** parancsmag időtartomány-helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2c587-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2c587-110">Egy elem biztonsági mentése után egy **AzRecoveryServicesBackupRecoveryLogChain** -objektumnak egy vagy több helyreállítási időtartománya van.</span><span class="sxs-lookup"><span data-stu-id="2c587-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2c587-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2c587-111">EXAMPLES</span></span>

### <span data-ttu-id="2c587-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c587-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2c587-113">Az első parancs hét nappal ezelőtt kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2c587-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2c587-114">A második parancs a mai dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2c587-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2c587-115">A harmadik parancs AzureWorkload kapja a biztonsági másolat tárolóját, és a $Container változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="2c587-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="2c587-116">A negyedik parancs a biztonsági másolatot kapja, majd a vezetékes parancsmagban a Backup Item objektumként osztja meg.</span><span class="sxs-lookup"><span data-stu-id="2c587-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="2c587-117">Az utolsó parancs a $BackupItemben található elem helyreállítási pontjának időtartományai sorát kapja, majd a $RP változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="2c587-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="2c587-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="2c587-118">Example 2</span></span>

<span data-ttu-id="2c587-119">Ez a parancs felsorolja a biztonsági másolatban szereplő töretlen log-elem kezdési és befejezési pontját.</span><span class="sxs-lookup"><span data-stu-id="2c587-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2c587-120">autogenerated</span><span class="sxs-lookup"><span data-stu-id="2c587-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="2c587-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c587-121">PARAMETERS</span></span>

### <span data-ttu-id="2c587-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c587-122">-DefaultProfile</span></span>
<span data-ttu-id="2c587-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c587-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c587-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2c587-124">-EndDate</span></span>
<span data-ttu-id="2c587-125">Annak a időtartománynak a záró időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="2c587-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c587-126">-Elem</span><span class="sxs-lookup"><span data-stu-id="2c587-126">-Item</span></span>
<span data-ttu-id="2c587-127">Védett elem objektum, amelynek helyreállítási pontját le kell olvasni</span><span class="sxs-lookup"><span data-stu-id="2c587-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c587-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2c587-128">-StartDate</span></span>
<span data-ttu-id="2c587-129">Az időtartomány kezdési időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="2c587-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c587-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2c587-130">-VaultId</span></span>
<span data-ttu-id="2c587-131">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="2c587-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2c587-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c587-132">CommonParameters</span></span>
<span data-ttu-id="2c587-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c587-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c587-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c587-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c587-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c587-135">INPUTS</span></span>

### <span data-ttu-id="2c587-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2c587-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2c587-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2c587-137">System.String</span></span>

## <span data-ttu-id="2c587-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c587-138">OUTPUTS</span></span>

### <span data-ttu-id="2c587-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2c587-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2c587-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c587-140">NOTES</span></span>

## <span data-ttu-id="2c587-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c587-141">RELATED LINKS</span></span>
