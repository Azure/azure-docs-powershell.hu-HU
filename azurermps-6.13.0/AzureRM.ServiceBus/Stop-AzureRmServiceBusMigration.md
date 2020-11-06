---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497304"
---
# <span data-ttu-id="11e22-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="11e22-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="11e22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11e22-102">SYNOPSIS</span></span>
<span data-ttu-id="11e22-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="11e22-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11e22-104">SYNTAX</span></span>

### <span data-ttu-id="11e22-105">MigrationConfigurationPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11e22-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e22-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11e22-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e22-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e22-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e22-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11e22-108">DESCRIPTION</span></span>
<span data-ttu-id="11e22-109">A **stop-AzureRmServiceBusMigration** parancsmagok a standard és a prémium névtér közötti áttelepítést tremitates</span><span class="sxs-lookup"><span data-stu-id="11e22-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="11e22-110">Példák</span><span class="sxs-lookup"><span data-stu-id="11e22-110">EXAMPLES</span></span>

### <span data-ttu-id="11e22-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11e22-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="11e22-112">a parancsmag a szokásos névtér és prémium névtér termitates áttelepítését biztosítja az áttelepítési konfiguráció létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="11e22-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="11e22-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11e22-113">PARAMETERS</span></span>

### <span data-ttu-id="11e22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e22-114">-DefaultProfile</span></span>
<span data-ttu-id="11e22-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11e22-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e22-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e22-116">-InputObject</span></span>
<span data-ttu-id="11e22-117">A szolgáltatás busz áttelepítésének konfigurációs standard Namespace objektuma</span><span class="sxs-lookup"><span data-stu-id="11e22-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="11e22-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11e22-118">-Name</span></span>
<span data-ttu-id="11e22-119">Szokásos névtér neve</span><span class="sxs-lookup"><span data-stu-id="11e22-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="11e22-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11e22-120">-PassThru</span></span>
<span data-ttu-id="11e22-121">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="11e22-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="11e22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e22-122">-ResourceGroupName</span></span>
<span data-ttu-id="11e22-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="11e22-123">Resource Group Name</span></span>

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

### <span data-ttu-id="11e22-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e22-124">-ResourceId</span></span>
<span data-ttu-id="11e22-125">A szolgáltatás busz áttelepítésének konfigurációja standard Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="11e22-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="11e22-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11e22-126">-Confirm</span></span>
<span data-ttu-id="11e22-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11e22-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e22-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e22-128">-WhatIf</span></span>
<span data-ttu-id="11e22-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11e22-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e22-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11e22-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e22-131">CommonParameters</span></span>
<span data-ttu-id="11e22-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11e22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e22-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e22-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e22-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e22-134">INPUTS</span></span>

### <span data-ttu-id="11e22-135">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="11e22-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="11e22-136">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11e22-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="11e22-137">System. String</span><span class="sxs-lookup"><span data-stu-id="11e22-137">System.String</span></span>

## <span data-ttu-id="11e22-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e22-138">OUTPUTS</span></span>

### <span data-ttu-id="11e22-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11e22-139">System.Boolean</span></span>

## <span data-ttu-id="11e22-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11e22-140">NOTES</span></span>

## <span data-ttu-id="11e22-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11e22-141">RELATED LINKS</span></span>
