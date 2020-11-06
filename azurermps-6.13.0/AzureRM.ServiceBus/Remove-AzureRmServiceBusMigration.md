---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494911"
---
# <span data-ttu-id="0fe3a-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0fe3a-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="0fe3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fe3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe3a-103">Parancsmag – a standardtól a prémium névterekhez való áttelepítési konfiguráció törlése</span><span class="sxs-lookup"><span data-stu-id="0fe3a-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fe3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fe3a-104">SYNTAX</span></span>

### <span data-ttu-id="0fe3a-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fe3a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe3a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0fe3a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe3a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe3a-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe3a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fe3a-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe3a-109">A **Remove-AzureRmServiceBusMigration** parancsmag a standard prémium névterekhez való áttelepítési konfigurációját törli</span><span class="sxs-lookup"><span data-stu-id="0fe3a-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="0fe3a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0fe3a-110">EXAMPLES</span></span>

### <span data-ttu-id="0fe3a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fe3a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="0fe3a-112">A "TestingNamespaceStandardMirgation" áttelepítési konfiguráció törlése</span><span class="sxs-lookup"><span data-stu-id="0fe3a-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="0fe3a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fe3a-113">PARAMETERS</span></span>

### <span data-ttu-id="0fe3a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fe3a-114">-AsJob</span></span>
<span data-ttu-id="0fe3a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0fe3a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fe3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe3a-116">-DefaultProfile</span></span>
<span data-ttu-id="0fe3a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fe3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe3a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe3a-118">-InputObject</span></span>
<span data-ttu-id="0fe3a-119">A szolgáltatás busz áttelepítése standard Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="0fe3a-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="0fe3a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fe3a-120">-Name</span></span>
<span data-ttu-id="0fe3a-121">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="0fe3a-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="0fe3a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fe3a-122">-PassThru</span></span>
<span data-ttu-id="0fe3a-123">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="0fe3a-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0fe3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fe3a-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0fe3a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0fe3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe3a-126">-ResourceId</span></span>
<span data-ttu-id="0fe3a-127">A szolgáltatás busz áttelepítése standard Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="0fe3a-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="0fe3a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fe3a-128">-Confirm</span></span>
<span data-ttu-id="0fe3a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fe3a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe3a-130">-WhatIf</span></span>
<span data-ttu-id="0fe3a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fe3a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe3a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fe3a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe3a-133">CommonParameters</span></span>
<span data-ttu-id="0fe3a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fe3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe3a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe3a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fe3a-136">INPUTS</span></span>

### <span data-ttu-id="0fe3a-137">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0fe3a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="0fe3a-138">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0fe3a-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0fe3a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe3a-139">System.String</span></span>

## <span data-ttu-id="0fe3a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fe3a-140">OUTPUTS</span></span>

### <span data-ttu-id="0fe3a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fe3a-141">System.Boolean</span></span>

## <span data-ttu-id="0fe3a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fe3a-142">NOTES</span></span>

## <span data-ttu-id="0fe3a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fe3a-143">RELATED LINKS</span></span>
