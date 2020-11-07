---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669134"
---
# <span data-ttu-id="c5d9e-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c5d9e-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="c5d9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d9e-103">Új áttelepítési konfigurációt hoz létre, és elindítja az entitások áttelepítését a standardtól a prémium névtérig</span><span class="sxs-lookup"><span data-stu-id="c5d9e-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="c5d9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5d9e-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5d9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d9e-106">A **Start-AzServiceBusMigration** parancsmag új áttelepítési konfigurációt hoz létre, és elindítja az entitások áttelepítését a szokásostól a prémium névtérig</span><span class="sxs-lookup"><span data-stu-id="c5d9e-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="c5d9e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d9e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c5d9e-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="c5d9e-109">Új áttelepítési konfiguráció létrehozása "TestingNamespaceStandardMirgation"-hoz ' TestingNamespacePremiumMirgation ' névterekhez</span><span class="sxs-lookup"><span data-stu-id="c5d9e-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="c5d9e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="c5d9e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5d9e-111">-AsJob</span></span>
<span data-ttu-id="c5d9e-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5d9e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5d9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d9e-113">-DefaultProfile</span></span>
<span data-ttu-id="c5d9e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d9e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5d9e-115">-Name</span></span>
<span data-ttu-id="c5d9e-116">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="c5d9e-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="c5d9e-117">-PostMigrationName</span></span>
<span data-ttu-id="c5d9e-118">Áttelepítési név közzététele a standrad-névtérben az áttelepítés során</span><span class="sxs-lookup"><span data-stu-id="c5d9e-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5d9e-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c5d9e-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="c5d9e-121">-TargetNameSpace</span></span>
<span data-ttu-id="c5d9e-122">Prémium névtér-azonosító</span><span class="sxs-lookup"><span data-stu-id="c5d9e-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5d9e-123">-Confirm</span></span>
<span data-ttu-id="c5d9e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d9e-125">-WhatIf</span></span>
<span data-ttu-id="c5d9e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d9e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d9e-128">CommonParameters</span></span>
<span data-ttu-id="c5d9e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5d9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d9e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5d9e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d9e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5d9e-131">INPUTS</span></span>

### <span data-ttu-id="c5d9e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5d9e-132">None</span></span>

## <span data-ttu-id="c5d9e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5d9e-133">OUTPUTS</span></span>

### <span data-ttu-id="c5d9e-134">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c5d9e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c5d9e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5d9e-135">NOTES</span></span>

## <span data-ttu-id="c5d9e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5d9e-136">RELATED LINKS</span></span>
