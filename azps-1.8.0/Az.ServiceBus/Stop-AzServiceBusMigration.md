---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: c507caa0ce6697132876309a7ae816802a682683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669132"
---
# <span data-ttu-id="3aa48-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3aa48-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="3aa48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3aa48-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa48-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="3aa48-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="3aa48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3aa48-104">SYNTAX</span></span>

### <span data-ttu-id="3aa48-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3aa48-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa48-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3aa48-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa48-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa48-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aa48-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3aa48-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa48-109">A **stop-AzServiceBusMigration** parancsmagok lemondják a standard és a prémium névtér közötti áttelepítést.</span><span class="sxs-lookup"><span data-stu-id="3aa48-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="3aa48-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3aa48-110">EXAMPLES</span></span>

### <span data-ttu-id="3aa48-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3aa48-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="3aa48-112">Parancsmag – az áttelepítési konfiguráció létrehozásakor a standard névtér és prémium névtér közötti áttelepítés befejezése.</span><span class="sxs-lookup"><span data-stu-id="3aa48-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="3aa48-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3aa48-113">PARAMETERS</span></span>

### <span data-ttu-id="3aa48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa48-114">-DefaultProfile</span></span>
<span data-ttu-id="3aa48-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3aa48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa48-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa48-116">-InputObject</span></span>
<span data-ttu-id="3aa48-117">A szolgáltatás busz áttelepítésének konfigurációs standard Namespace objektuma</span><span class="sxs-lookup"><span data-stu-id="3aa48-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="3aa48-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3aa48-118">-Name</span></span>
<span data-ttu-id="3aa48-119">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="3aa48-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="3aa48-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aa48-120">-PassThru</span></span>
<span data-ttu-id="3aa48-121">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="3aa48-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3aa48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa48-122">-ResourceGroupName</span></span>
<span data-ttu-id="3aa48-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3aa48-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa48-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa48-124">-ResourceId</span></span>
<span data-ttu-id="3aa48-125">A szolgáltatás busz áttelepítésének konfigurációja standard Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="3aa48-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="3aa48-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3aa48-126">-Confirm</span></span>
<span data-ttu-id="3aa48-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3aa48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa48-128">-WhatIf</span></span>
<span data-ttu-id="3aa48-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3aa48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa48-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3aa48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa48-131">CommonParameters</span></span>
<span data-ttu-id="3aa48-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3aa48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa48-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa48-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa48-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3aa48-134">INPUTS</span></span>

### <span data-ttu-id="3aa48-135">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3aa48-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="3aa48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3aa48-136">System.String</span></span>

## <span data-ttu-id="3aa48-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3aa48-137">OUTPUTS</span></span>

### <span data-ttu-id="3aa48-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3aa48-138">System.Boolean</span></span>

## <span data-ttu-id="3aa48-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3aa48-139">NOTES</span></span>

## <span data-ttu-id="3aa48-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3aa48-140">RELATED LINKS</span></span>
