---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208102"
---
# <span data-ttu-id="9333e-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9333e-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="9333e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9333e-102">SYNOPSIS</span></span>
<span data-ttu-id="9333e-103">Új áttelepítési konfigurációt hoz létre, és megkezdi az entitások áttelepítését a Standardról a Prémium névterekbe</span><span class="sxs-lookup"><span data-stu-id="9333e-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="9333e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9333e-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9333e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9333e-105">DESCRIPTION</span></span>
<span data-ttu-id="9333e-106">A **Start-AzServiceBusMigration** parancsmag létrehoz egy új áttelepítési konfigurációt, és megkezdi az entitások áttelepítését a Standardból a Prémium névterekbe</span><span class="sxs-lookup"><span data-stu-id="9333e-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="9333e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9333e-107">EXAMPLES</span></span>

### <span data-ttu-id="9333e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9333e-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="9333e-109">Új áttelepítési konfigurációt hoz létre a "TestingNamespaceStandardMigration" és a "TestingNamespacePremiumMigration" névterek számára.</span><span class="sxs-lookup"><span data-stu-id="9333e-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="9333e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9333e-110">PARAMETERS</span></span>

### <span data-ttu-id="9333e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9333e-111">-AsJob</span></span>
<span data-ttu-id="9333e-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9333e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9333e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9333e-113">-DefaultProfile</span></span>
<span data-ttu-id="9333e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9333e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9333e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9333e-115">-Name</span></span>
<span data-ttu-id="9333e-116">Normál névtérnév</span><span class="sxs-lookup"><span data-stu-id="9333e-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="9333e-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="9333e-117">-PostMigrationName</span></span>
<span data-ttu-id="9333e-118">Áttelepítés utáni név a szokásos névtérhez az áttelepítésben</span><span class="sxs-lookup"><span data-stu-id="9333e-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="9333e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9333e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9333e-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9333e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="9333e-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="9333e-121">-TargetNameSpace</span></span>
<span data-ttu-id="9333e-122">Premium Namespace ARM Id</span><span class="sxs-lookup"><span data-stu-id="9333e-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="9333e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9333e-123">-Confirm</span></span>
<span data-ttu-id="9333e-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9333e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9333e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9333e-125">-WhatIf</span></span>
<span data-ttu-id="9333e-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9333e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9333e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9333e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9333e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9333e-128">CommonParameters</span></span>
<span data-ttu-id="9333e-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9333e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9333e-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9333e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9333e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9333e-131">INPUTS</span></span>

### <span data-ttu-id="9333e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9333e-132">None</span></span>

## <span data-ttu-id="9333e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9333e-133">OUTPUTS</span></span>

### <span data-ttu-id="9333e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9333e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="9333e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9333e-135">NOTES</span></span>

## <span data-ttu-id="9333e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9333e-136">RELATED LINKS</span></span>
