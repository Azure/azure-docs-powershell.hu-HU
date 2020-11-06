---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494736"
---
# <span data-ttu-id="651c7-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="651c7-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="651c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="651c7-102">SYNOPSIS</span></span>
<span data-ttu-id="651c7-103">Az ASR-védelemmel ellátott elemek replikálásának engedélyezése replikációs védelemmel ellátott elem létrehozásával</span><span class="sxs-lookup"><span data-stu-id="651c7-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="651c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="651c7-104">SYNTAX</span></span>

### <span data-ttu-id="651c7-105">Letiltó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="651c7-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="651c7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="651c7-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="651c7-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="651c7-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="651c7-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="651c7-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="651c7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="651c7-109">DESCRIPTION</span></span>
<span data-ttu-id="651c7-110">A **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="651c7-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="651c7-111">Ezzel a parancsmaggal engedélyezheti az ASR-védelemmel ellátott elemek replikálását.</span><span class="sxs-lookup"><span data-stu-id="651c7-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="651c7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="651c7-112">EXAMPLES</span></span>

### <span data-ttu-id="651c7-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="651c7-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="651c7-114">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="651c7-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="651c7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="651c7-115">PARAMETERS</span></span>

### <span data-ttu-id="651c7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="651c7-116">-Name</span></span>
<span data-ttu-id="651c7-117">Az ASR replikációs szolgáltatása által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="651c7-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-118">-OS</span><span class="sxs-lookup"><span data-stu-id="651c7-118">-OS</span></span>
<span data-ttu-id="651c7-119">Az operációs rendszer családját adja meg.</span><span class="sxs-lookup"><span data-stu-id="651c7-119">Specifies the operating system family.</span></span>
<span data-ttu-id="651c7-120">A paraméter elfogadható értékei a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="651c7-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="651c7-121">-OSDiskName</span></span>
<span data-ttu-id="651c7-122">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="651c7-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="651c7-123">-ProtectableItem</span></span>
<span data-ttu-id="651c7-124">Annak az ASR-elemnek az objektumát adja meg, amelyhez a replikáció engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="651c7-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="651c7-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="651c7-126">Az ASR-védelmi tároló társítása objektum, amely megfelel a replikációhoz használandó replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="651c7-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="651c7-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="651c7-128">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="651c7-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="651c7-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="651c7-130">Meghatározza annak az erőforráscsoport-azonosítónak az azonosítóját, amelyben a virtuális gépet feladatátvétel esetén létrehozzák.</span><span class="sxs-lookup"><span data-stu-id="651c7-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651c7-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="651c7-131">-WaitForCompletion</span></span>
<span data-ttu-id="651c7-132">Azt adja meg, hogy a parancsmagnak a művelet befejezésekor várnia kell.</span><span class="sxs-lookup"><span data-stu-id="651c7-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="651c7-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="651c7-133">-Confirm</span></span>
<span data-ttu-id="651c7-134">Megerősítés kérése a művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="651c7-134">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="651c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="651c7-135">-WhatIf</span></span>
<span data-ttu-id="651c7-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="651c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="651c7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="651c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="651c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651c7-138">CommonParameters</span></span>
<span data-ttu-id="651c7-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="651c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651c7-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651c7-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="651c7-141">INPUTS</span></span>

### <span data-ttu-id="651c7-142">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="651c7-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="651c7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="651c7-143">OUTPUTS</span></span>

### <span data-ttu-id="651c7-144">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="651c7-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="651c7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="651c7-145">NOTES</span></span>

## <span data-ttu-id="651c7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="651c7-146">RELATED LINKS</span></span>

[<span data-ttu-id="651c7-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="651c7-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="651c7-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="651c7-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="651c7-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="651c7-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
