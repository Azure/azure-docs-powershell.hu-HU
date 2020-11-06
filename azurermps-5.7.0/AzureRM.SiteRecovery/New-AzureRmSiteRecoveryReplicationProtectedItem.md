---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502368"
---
# <span data-ttu-id="1b729-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b729-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="1b729-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b729-102">SYNOPSIS</span></span>
<span data-ttu-id="1b729-103">Védelemmel ellátott elem replikálásának engedélyezése védett elemek létrehozásával</span><span class="sxs-lookup"><span data-stu-id="1b729-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b729-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b729-104">SYNTAX</span></span>

### <span data-ttu-id="1b729-105">Letiltó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b729-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b729-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1b729-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b729-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1b729-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b729-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="1b729-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b729-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b729-109">DESCRIPTION</span></span>
<span data-ttu-id="1b729-110">A **New-AzureRmSiteRecoveryReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1b729-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="1b729-111">Ezzel a parancsmaggal engedélyezheti a védett elemek replikálását.</span><span class="sxs-lookup"><span data-stu-id="1b729-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="1b729-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1b729-112">EXAMPLES</span></span>

## <span data-ttu-id="1b729-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b729-113">PARAMETERS</span></span>

### <span data-ttu-id="1b729-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b729-114">-DefaultProfile</span></span>
<span data-ttu-id="1b729-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b729-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b729-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1b729-116">-Name</span></span>
<span data-ttu-id="1b729-117">Az Azure webhely-helyreállítási replikációs szolgáltatással védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b729-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

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

### <span data-ttu-id="1b729-118">-OS</span><span class="sxs-lookup"><span data-stu-id="1b729-118">-OS</span></span>
<span data-ttu-id="1b729-119">Az operációs rendszer családját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b729-119">Specifies the operating system family.</span></span>
<span data-ttu-id="1b729-120">A paraméter elfogadható értékei a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="1b729-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="1b729-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="1b729-121">-OSDiskName</span></span>
<span data-ttu-id="1b729-122">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b729-122">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="1b729-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1b729-123">-ProtectableItem</span></span>
<span data-ttu-id="1b729-124">Az Azure webhely-helyreállítási védelemmel ellátott elemét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b729-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

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

### <span data-ttu-id="1b729-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1b729-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="1b729-126">Megadja az Azure webhely-helyreállítási védelem tárolójának a replikáláshoz használandó objektumát.</span><span class="sxs-lookup"><span data-stu-id="1b729-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

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

### <span data-ttu-id="1b729-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1b729-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="1b729-128">Annak az Azure-tárterületnek az AZONOSÍTÓját adja meg, amelyre a parancsmag replikálja.</span><span class="sxs-lookup"><span data-stu-id="1b729-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

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

### <span data-ttu-id="1b729-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1b729-129">-WaitForCompletion</span></span>
<span data-ttu-id="1b729-130">Azt jelzi, hogy a parancsmag a befejezésre vár.</span><span class="sxs-lookup"><span data-stu-id="1b729-130">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="1b729-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b729-131">-Confirm</span></span>
<span data-ttu-id="1b729-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b729-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b729-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b729-133">-WhatIf</span></span>
<span data-ttu-id="1b729-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b729-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1b729-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b729-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b729-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b729-136">CommonParameters</span></span>
<span data-ttu-id="1b729-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b729-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b729-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b729-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b729-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b729-139">INPUTS</span></span>

### <span data-ttu-id="1b729-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1b729-140">ASRProtectableItem</span></span>
<span data-ttu-id="1b729-141">A ' ProtectableItem ' paraméter az "ASRProtectableItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1b729-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="1b729-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b729-142">OUTPUTS</span></span>

### <span data-ttu-id="1b729-143">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1b729-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1b729-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b729-144">NOTES</span></span>

## <span data-ttu-id="1b729-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b729-145">RELATED LINKS</span></span>

[<span data-ttu-id="1b729-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b729-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1b729-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b729-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1b729-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b729-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
