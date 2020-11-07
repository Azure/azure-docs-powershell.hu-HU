---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679925"
---
# <span data-ttu-id="6158f-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="6158f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6158f-102">SYNOPSIS</span></span>
<span data-ttu-id="6158f-103">Az Azure webhely-helyreállítási replikációval védett elem eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6158f-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6158f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6158f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6158f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6158f-105">DESCRIPTION</span></span>
<span data-ttu-id="6158f-106">A **Remove-AzureRmSiteRecoveryReplicationProtectedItem** parancsmag eltávolítja az Azure site Recovery Replication védett elemét.</span><span class="sxs-lookup"><span data-stu-id="6158f-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="6158f-107">A művelet hatására a replikáció leáll a védett elemen.</span><span class="sxs-lookup"><span data-stu-id="6158f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="6158f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6158f-108">EXAMPLES</span></span>

## <span data-ttu-id="6158f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6158f-109">PARAMETERS</span></span>

### <span data-ttu-id="6158f-110">-Force</span><span class="sxs-lookup"><span data-stu-id="6158f-110">-Force</span></span>
<span data-ttu-id="6158f-111">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6158f-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6158f-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6158f-113">A replikációs védelemmel ellátott elem objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6158f-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6158f-114">-WaitForCompletion</span></span>
<span data-ttu-id="6158f-115">Azt jelzi, hogy a parancsmag megvárja a művelet befejezését.</span><span class="sxs-lookup"><span data-stu-id="6158f-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="6158f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6158f-116">-Confirm</span></span>
<span data-ttu-id="6158f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6158f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6158f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6158f-118">-WhatIf</span></span>
<span data-ttu-id="6158f-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6158f-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6158f-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6158f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6158f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6158f-121">-DefaultProfile</span></span>
<span data-ttu-id="6158f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6158f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6158f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6158f-123">CommonParameters</span></span>
<span data-ttu-id="6158f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6158f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6158f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6158f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6158f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6158f-126">INPUTS</span></span>

### <span data-ttu-id="6158f-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="6158f-128">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6158f-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="6158f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6158f-129">OUTPUTS</span></span>

### <span data-ttu-id="6158f-130">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6158f-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6158f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6158f-131">NOTES</span></span>

## <span data-ttu-id="6158f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6158f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6158f-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6158f-134">Új – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6158f-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6158f-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
