---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335873"
---
# <span data-ttu-id="1550b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="1550b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="1550b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1550b-102">SYNOPSIS</span></span>
<span data-ttu-id="1550b-103">Eltávolítja a lemezeket a replikációval védett elemhez.</span><span class="sxs-lookup"><span data-stu-id="1550b-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="1550b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1550b-104">SYNTAX</span></span>

### <span data-ttu-id="1550b-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1550b-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1550b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1550b-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1550b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1550b-107">DESCRIPTION</span></span>
<span data-ttu-id="1550b-108">A **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** parancsmag eltávolítja a lemezt az ASR-replikációval védett elemből.</span><span class="sxs-lookup"><span data-stu-id="1550b-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="1550b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1550b-109">EXAMPLES</span></span>

### <span data-ttu-id="1550b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1550b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="1550b-111">Indítsa el azt a műveletet, amely eltávolítja a megadott lemezt a nem védett lemez védett virtuális gépe elől.</span><span class="sxs-lookup"><span data-stu-id="1550b-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="1550b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1550b-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="1550b-113">Indítsa el a műveletet a felügyelt lemez védett virtuális gépének adott lemezről való eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="1550b-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="1550b-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="1550b-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="1550b-115">Elindítja a műveletet a megadott lemez eltávolításához, és visszaadja a védett lemez eltávolítása művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="1550b-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="1550b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1550b-116">PARAMETERS</span></span>

### <span data-ttu-id="1550b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1550b-117">-Confirm</span></span>
<span data-ttu-id="1550b-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1550b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1550b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1550b-119">-DefaultProfile</span></span>
<span data-ttu-id="1550b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1550b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1550b-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="1550b-121">-DiskId</span></span>
<span data-ttu-id="1550b-122">A felügyelt lemezazonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1550b-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="1550b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1550b-123">-InputObject</span></span>
<span data-ttu-id="1550b-124">A parancsmag bemeneti objektuma: A ASR replikációs védett elemobjektuma, amelynek a lemezét el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="1550b-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="1550b-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="1550b-125">-VhdUri</span></span>
<span data-ttu-id="1550b-126">A vhd Uri-nak a listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1550b-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="1550b-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1550b-127">-WaitForCompletion</span></span>
<span data-ttu-id="1550b-128">Várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="1550b-128">Wait For Completion</span></span>

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

### <span data-ttu-id="1550b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1550b-129">-WhatIf</span></span>
<span data-ttu-id="1550b-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1550b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1550b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1550b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1550b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1550b-132">CommonParameters</span></span>
<span data-ttu-id="1550b-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1550b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1550b-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1550b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1550b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1550b-135">INPUTS</span></span>

### <span data-ttu-id="1550b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1550b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1550b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1550b-137">OUTPUTS</span></span>

### <span data-ttu-id="1550b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="1550b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1550b-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1550b-139">NOTES</span></span>

## <span data-ttu-id="1550b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1550b-140">RELATED LINKS</span></span>
