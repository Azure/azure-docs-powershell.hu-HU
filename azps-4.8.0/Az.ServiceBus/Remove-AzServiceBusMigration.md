---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182153"
---
# <span data-ttu-id="05c80-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="05c80-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="05c80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05c80-102">SYNOPSIS</span></span>
<span data-ttu-id="05c80-103">Parancsmag – a standardtól a prémium névterekhez való áttelepítési konfiguráció törlése</span><span class="sxs-lookup"><span data-stu-id="05c80-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="05c80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05c80-104">SYNTAX</span></span>

### <span data-ttu-id="05c80-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05c80-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c80-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05c80-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c80-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c80-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c80-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05c80-108">DESCRIPTION</span></span>
<span data-ttu-id="05c80-109">A **Remove-AzServiceBusMigration** parancsmag a standard prémium névterekhez való áttelepítési konfigurációját törli</span><span class="sxs-lookup"><span data-stu-id="05c80-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="05c80-110">Példák</span><span class="sxs-lookup"><span data-stu-id="05c80-110">EXAMPLES</span></span>

### <span data-ttu-id="05c80-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05c80-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="05c80-112">A "TestingNamespaceStandardMigration" áttelepítési konfiguráció törlése</span><span class="sxs-lookup"><span data-stu-id="05c80-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="05c80-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05c80-113">PARAMETERS</span></span>

### <span data-ttu-id="05c80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05c80-114">-AsJob</span></span>
<span data-ttu-id="05c80-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="05c80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05c80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c80-116">-DefaultProfile</span></span>
<span data-ttu-id="05c80-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05c80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c80-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05c80-118">-InputObject</span></span>
<span data-ttu-id="05c80-119">A szolgáltatás busz áttelepítése standard Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="05c80-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="05c80-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05c80-120">-Name</span></span>
<span data-ttu-id="05c80-121">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="05c80-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="05c80-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05c80-122">-PassThru</span></span>
<span data-ttu-id="05c80-123">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="05c80-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="05c80-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c80-124">-ResourceGroupName</span></span>
<span data-ttu-id="05c80-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="05c80-125">Resource Group Name</span></span>

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

### <span data-ttu-id="05c80-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05c80-126">-ResourceId</span></span>
<span data-ttu-id="05c80-127">A szolgáltatás busz áttelepítése standard Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="05c80-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="05c80-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05c80-128">-Confirm</span></span>
<span data-ttu-id="05c80-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05c80-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c80-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c80-130">-WhatIf</span></span>
<span data-ttu-id="05c80-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05c80-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c80-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05c80-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c80-133">CommonParameters</span></span>
<span data-ttu-id="05c80-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05c80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c80-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c80-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c80-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c80-136">INPUTS</span></span>

### <span data-ttu-id="05c80-137">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="05c80-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="05c80-138">System. String</span><span class="sxs-lookup"><span data-stu-id="05c80-138">System.String</span></span>

## <span data-ttu-id="05c80-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c80-139">OUTPUTS</span></span>

### <span data-ttu-id="05c80-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05c80-140">System.Boolean</span></span>

## <span data-ttu-id="05c80-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05c80-141">NOTES</span></span>

## <span data-ttu-id="05c80-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05c80-142">RELATED LINKS</span></span>
