---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493353"
---
# <span data-ttu-id="af5d1-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="af5d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="af5d1-103">Védelemmel ellátott elem replikálásának engedélyezése védett elemek létrehozásával</span><span class="sxs-lookup"><span data-stu-id="af5d1-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af5d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af5d1-104">SYNTAX</span></span>

### <span data-ttu-id="af5d1-105">Letiltó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af5d1-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5d1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="af5d1-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5d1-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="af5d1-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5d1-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="af5d1-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5d1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="af5d1-109">DESCRIPTION</span></span>
<span data-ttu-id="af5d1-110">A **New-AzureRmSiteRecoveryReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="af5d1-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="af5d1-111">Ezzel a parancsmaggal engedélyezheti a védett elemek replikálását.</span><span class="sxs-lookup"><span data-stu-id="af5d1-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="af5d1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="af5d1-112">EXAMPLES</span></span>

## <span data-ttu-id="af5d1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af5d1-113">PARAMETERS</span></span>

### <span data-ttu-id="af5d1-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af5d1-114">-Name</span></span>
<span data-ttu-id="af5d1-115">Az Azure webhely-helyreállítási replikációs szolgáltatással védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af5d1-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-116">-OS</span><span class="sxs-lookup"><span data-stu-id="af5d1-116">-OS</span></span>
<span data-ttu-id="af5d1-117">Az operációs rendszer családját adja meg.</span><span class="sxs-lookup"><span data-stu-id="af5d1-117">Specifies the operating system family.</span></span>
<span data-ttu-id="af5d1-118">A paraméter elfogadható értékei a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="af5d1-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="af5d1-119">-OSDiskName</span></span>
<span data-ttu-id="af5d1-120">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af5d1-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-121">-ProtectableItem</span></span>
<span data-ttu-id="af5d1-122">Az Azure webhely-helyreállítási védelemmel ellátott elemét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af5d1-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="af5d1-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="af5d1-124">Megadja az Azure webhely-helyreállítási védelem tárolójának a replikáláshoz használandó objektumát.</span><span class="sxs-lookup"><span data-stu-id="af5d1-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="af5d1-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="af5d1-126">Annak az Azure-tárterületnek az AZONOSÍTÓját adja meg, amelyre a parancsmag replikálja.</span><span class="sxs-lookup"><span data-stu-id="af5d1-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="af5d1-127">-WaitForCompletion</span></span>
<span data-ttu-id="af5d1-128">Azt jelzi, hogy a parancsmag a befejezésre vár.</span><span class="sxs-lookup"><span data-stu-id="af5d1-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af5d1-129">-Confirm</span></span>
<span data-ttu-id="af5d1-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af5d1-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5d1-131">-WhatIf</span></span>
<span data-ttu-id="af5d1-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af5d1-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="af5d1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af5d1-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5d1-134">-DefaultProfile</span></span>
<span data-ttu-id="af5d1-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af5d1-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af5d1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5d1-136">CommonParameters</span></span>
<span data-ttu-id="af5d1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af5d1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5d1-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af5d1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5d1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af5d1-139">INPUTS</span></span>

### <span data-ttu-id="af5d1-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-140">ASRProtectableItem</span></span>
<span data-ttu-id="af5d1-141">A ' ProtectableItem ' paraméter az "ASRProtectableItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="af5d1-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="af5d1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af5d1-142">OUTPUTS</span></span>

### <span data-ttu-id="af5d1-143">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af5d1-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af5d1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af5d1-144">NOTES</span></span>

## <span data-ttu-id="af5d1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af5d1-145">RELATED LINKS</span></span>

[<span data-ttu-id="af5d1-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="af5d1-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="af5d1-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="af5d1-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
