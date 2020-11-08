---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188033"
---
# <span data-ttu-id="c9170-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="c9170-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="c9170-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9170-102">SYNOPSIS</span></span>
<span data-ttu-id="c9170-103">Eltávolítja a lemezeket a replikációs védelemmel ellátott elemekhez.</span><span class="sxs-lookup"><span data-stu-id="c9170-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="c9170-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9170-104">SYNTAX</span></span>

### <span data-ttu-id="c9170-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9170-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9170-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c9170-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9170-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9170-107">DESCRIPTION</span></span>
<span data-ttu-id="c9170-108">A **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** parancsmag eltávolítja a lemezt az ASR-replikációs védelemmel ellátott elemből.</span><span class="sxs-lookup"><span data-stu-id="c9170-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="c9170-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9170-109">EXAMPLES</span></span>

### <span data-ttu-id="c9170-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9170-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="c9170-111">Indítsa el a műveletet, ha a nem felügyelt lemezekre vonatkozóan eltávolítja a megadott lemezt a VM védelmi szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="c9170-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="c9170-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9170-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="c9170-113">Indítsa el a műveletet, ha a kezelt lemezről eltávolítja a megadott lemezt a védelmi VM-ből.</span><span class="sxs-lookup"><span data-stu-id="c9170-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="c9170-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9170-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="c9170-115">Elindítja a műveletet a megadott lemez eltávolításához, és visszaadja a védett lemezek eltávolítása művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="c9170-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="c9170-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9170-116">PARAMETERS</span></span>

### <span data-ttu-id="c9170-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9170-117">-Confirm</span></span>
<span data-ttu-id="c9170-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9170-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9170-119">-DefaultProfile</span></span>
<span data-ttu-id="c9170-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9170-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-121">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="c9170-121">-DiskId</span></span>
<span data-ttu-id="c9170-122">A felügyelt lemezvezérlő-azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9170-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9170-123">-InputObject</span></span>
<span data-ttu-id="c9170-124">A bemeneti objektum a parancsmag: az ASR replikációs szolgáltatással védett elem objektuma, amely megfelel a lemez eltávolításának.</span><span class="sxs-lookup"><span data-stu-id="c9170-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="c9170-125">-VhdUri</span></span>
<span data-ttu-id="c9170-126">A VHD-URI-azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9170-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c9170-127">-WaitForCompletion</span></span>
<span data-ttu-id="c9170-128">Várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="c9170-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9170-129">-WhatIf</span></span>
<span data-ttu-id="c9170-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9170-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9170-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9170-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9170-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9170-132">CommonParameters</span></span>
<span data-ttu-id="c9170-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9170-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9170-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9170-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9170-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9170-135">INPUTS</span></span>

### <span data-ttu-id="c9170-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c9170-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c9170-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9170-137">OUTPUTS</span></span>

### <span data-ttu-id="c9170-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c9170-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c9170-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9170-139">NOTES</span></span>

## <span data-ttu-id="c9170-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9170-140">RELATED LINKS</span></span>
