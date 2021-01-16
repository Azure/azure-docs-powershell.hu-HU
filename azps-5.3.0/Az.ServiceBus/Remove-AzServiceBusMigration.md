---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479633"
---
# <span data-ttu-id="31e70-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31e70-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="31e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e70-102">SYNOPSIS</span></span>
<span data-ttu-id="31e70-103">Parancsmag törli a Standard–Premium névterek áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="31e70-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="31e70-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31e70-104">SYNTAX</span></span>

### <span data-ttu-id="31e70-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31e70-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e70-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31e70-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e70-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31e70-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e70-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31e70-108">DESCRIPTION</span></span>
<span data-ttu-id="31e70-109">A **Remove-AzServiceBusMigration** parancsmag törli a Standard–Premium névterek áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="31e70-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="31e70-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31e70-110">EXAMPLES</span></span>

### <span data-ttu-id="31e70-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="31e70-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="31e70-112">A "TestingNamespaceStandardMigration" áttelepítési konfiguráció törlése</span><span class="sxs-lookup"><span data-stu-id="31e70-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="31e70-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e70-113">PARAMETERS</span></span>

### <span data-ttu-id="31e70-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31e70-114">-AsJob</span></span>
<span data-ttu-id="31e70-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="31e70-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31e70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e70-116">-DefaultProfile</span></span>
<span data-ttu-id="31e70-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31e70-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31e70-118">-InputObject</span></span>
<span data-ttu-id="31e70-119">Service Bus Migration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="31e70-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31e70-120">-Name</span><span class="sxs-lookup"><span data-stu-id="31e70-120">-Name</span></span>
<span data-ttu-id="31e70-121">Normál névtérnév</span><span class="sxs-lookup"><span data-stu-id="31e70-121">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e70-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31e70-122">-PassThru</span></span>
<span data-ttu-id="31e70-123">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="31e70-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="31e70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e70-124">-ResourceGroupName</span></span>
<span data-ttu-id="31e70-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="31e70-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e70-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31e70-126">-ResourceId</span></span>
<span data-ttu-id="31e70-127">Service Bus Migration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="31e70-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e70-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31e70-128">-Confirm</span></span>
<span data-ttu-id="31e70-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31e70-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e70-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e70-130">-WhatIf</span></span>
<span data-ttu-id="31e70-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="31e70-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e70-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31e70-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e70-133">CommonParameters</span></span>
<span data-ttu-id="31e70-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e70-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e70-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e70-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31e70-136">INPUTS</span></span>

### <span data-ttu-id="31e70-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="31e70-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="31e70-138">System.String</span><span class="sxs-lookup"><span data-stu-id="31e70-138">System.String</span></span>

## <span data-ttu-id="31e70-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31e70-139">OUTPUTS</span></span>

### <span data-ttu-id="31e70-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31e70-140">System.Boolean</span></span>

## <span data-ttu-id="31e70-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31e70-141">NOTES</span></span>

## <span data-ttu-id="31e70-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31e70-142">RELATED LINKS</span></span>
