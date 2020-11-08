---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185869"
---
# <span data-ttu-id="aea9f-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aea9f-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="aea9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aea9f-102">SYNOPSIS</span></span>
<span data-ttu-id="aea9f-103">Új áttelepítési konfigurációt hoz létre, és elindítja az entitások áttelepítését a standardtól a prémium névtérig</span><span class="sxs-lookup"><span data-stu-id="aea9f-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="aea9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aea9f-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aea9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aea9f-105">DESCRIPTION</span></span>
<span data-ttu-id="aea9f-106">A **Start-AzServiceBusMigration** parancsmag új áttelepítési konfigurációt hoz létre, és elindítja az entitások áttelepítését a szokásostól a prémium névtérig</span><span class="sxs-lookup"><span data-stu-id="aea9f-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="aea9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aea9f-107">EXAMPLES</span></span>

### <span data-ttu-id="aea9f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aea9f-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="aea9f-109">Új áttelepítési konfiguráció létrehozása "TestingNamespaceStandardMigration"-hoz ' TestingNamespacePremiumMigration ' névterekhez</span><span class="sxs-lookup"><span data-stu-id="aea9f-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="aea9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aea9f-110">PARAMETERS</span></span>

### <span data-ttu-id="aea9f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aea9f-111">-AsJob</span></span>
<span data-ttu-id="aea9f-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aea9f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aea9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea9f-113">-DefaultProfile</span></span>
<span data-ttu-id="aea9f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aea9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea9f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aea9f-115">-Name</span></span>
<span data-ttu-id="aea9f-116">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="aea9f-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="aea9f-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="aea9f-117">-PostMigrationName</span></span>
<span data-ttu-id="aea9f-118">A normál névtér áttelepítési nevének közzététele az áttelepítés során</span><span class="sxs-lookup"><span data-stu-id="aea9f-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="aea9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="aea9f-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="aea9f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="aea9f-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="aea9f-121">-TargetNameSpace</span></span>
<span data-ttu-id="aea9f-122">Prémium névtér-azonosító</span><span class="sxs-lookup"><span data-stu-id="aea9f-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="aea9f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aea9f-123">-Confirm</span></span>
<span data-ttu-id="aea9f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aea9f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea9f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea9f-125">-WhatIf</span></span>
<span data-ttu-id="aea9f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aea9f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea9f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aea9f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea9f-128">CommonParameters</span></span>
<span data-ttu-id="aea9f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aea9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea9f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea9f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea9f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea9f-131">INPUTS</span></span>

### <span data-ttu-id="aea9f-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="aea9f-132">None</span></span>

## <span data-ttu-id="aea9f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea9f-133">OUTPUTS</span></span>

### <span data-ttu-id="aea9f-134">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="aea9f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="aea9f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aea9f-135">NOTES</span></span>

## <span data-ttu-id="aea9f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aea9f-136">RELATED LINKS</span></span>
