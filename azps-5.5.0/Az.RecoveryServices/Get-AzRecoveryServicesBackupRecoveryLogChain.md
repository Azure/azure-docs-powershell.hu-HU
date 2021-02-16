---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146226"
---
# <span data-ttu-id="0a64f-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="0a64f-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="0a64f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a64f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a64f-103">Ez a parancs felsorolja az adott biztonságimásolat-elem töretlen naplóláncának kezdő és záró pontjait.</span><span class="sxs-lookup"><span data-stu-id="0a64f-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="0a64f-104">Segítségével megállapíthatja, hogy érvényes-e az az időpont, amelyre a felhasználó vissza szeretné állítani a adatbázis-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0a64f-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="0a64f-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a64f-105">SYNTAX</span></span>

### <span data-ttu-id="0a64f-106">NoFilterParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a64f-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a64f-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="0a64f-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a64f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a64f-108">DESCRIPTION</span></span>
<span data-ttu-id="0a64f-109">A **Get-AzRecoveryServicesBackupRecoveryLogChain** parancsmag időben megkapja az időtartomány helyreállítási pontjait egy biztonsági másolatként használt Azure Biztonsági másolat elemhez.</span><span class="sxs-lookup"><span data-stu-id="0a64f-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="0a64f-110">Miután biztonságiolt egy elemet, az **AzRecoveryServicesBackupRecoveryLogChain** objektumnak egy vagy több helyreállítási időtartománya van.</span><span class="sxs-lookup"><span data-stu-id="0a64f-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="0a64f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a64f-111">EXAMPLES</span></span>

### <span data-ttu-id="0a64f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a64f-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="0a64f-113">Az első parancs hét nappal ezelőtti dátumot ad vissza, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="0a64f-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="0a64f-114">A második parancs megkapja a mai dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="0a64f-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="0a64f-115">A harmadik parancs lekérte az AzureWorkload biztonságimásolat-tárolókat, és tárolja őket a $Container változóban.</span><span class="sxs-lookup"><span data-stu-id="0a64f-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="0a64f-116">A negyedik parancs megkapja a biztonságimásolat-elemet, majd megosztja azt a bevezető parancsmagon keresztül biztonságimásolat-elem objektumként.</span><span class="sxs-lookup"><span data-stu-id="0a64f-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="0a64f-117">Az utolsó parancs lekérte az elem helyreállítási időtartományának tömbét a $BackupItem, majd tárolja őket a $RP változóban.</span><span class="sxs-lookup"><span data-stu-id="0a64f-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="0a64f-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="0a64f-118">Example 2</span></span>

<span data-ttu-id="0a64f-119">Ez a parancs felsorolja az adott biztonságimásolat-elem töretlen naplóláncának kezdő és záró pontjait.</span><span class="sxs-lookup"><span data-stu-id="0a64f-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="0a64f-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="0a64f-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="0a64f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a64f-121">PARAMETERS</span></span>

### <span data-ttu-id="0a64f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a64f-122">-DefaultProfile</span></span>
<span data-ttu-id="0a64f-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a64f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a64f-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0a64f-124">-EndDate</span></span>
<span data-ttu-id="0a64f-125">Annak az időtartománynak a vége, amelynek helyreállítási pontját le kell kérni</span><span class="sxs-lookup"><span data-stu-id="0a64f-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0a64f-126">-Item</span><span class="sxs-lookup"><span data-stu-id="0a64f-126">-Item</span></span>
<span data-ttu-id="0a64f-127">Védett elem objektum, amelyhez helyreállítási pontot kell lehívni</span><span class="sxs-lookup"><span data-stu-id="0a64f-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0a64f-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0a64f-128">-StartDate</span></span>
<span data-ttu-id="0a64f-129">Annak az időtartománynak a kezdési ideje, amelyhez helyreállítási pontot kell lehívni</span><span class="sxs-lookup"><span data-stu-id="0a64f-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0a64f-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0a64f-130">-VaultId</span></span>
<span data-ttu-id="0a64f-131">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0a64f-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0a64f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a64f-132">CommonParameters</span></span>
<span data-ttu-id="0a64f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a64f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a64f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a64f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a64f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a64f-135">INPUTS</span></span>

### <span data-ttu-id="0a64f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="0a64f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="0a64f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0a64f-137">System.String</span></span>

## <span data-ttu-id="0a64f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a64f-138">OUTPUTS</span></span>

### <span data-ttu-id="0a64f-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="0a64f-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="0a64f-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a64f-140">NOTES</span></span>

## <span data-ttu-id="0a64f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a64f-141">RELATED LINKS</span></span>
