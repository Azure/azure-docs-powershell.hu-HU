---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 23c79f4ceed4e6b9dc537cb6e04fb602fd7a4bbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672876"
---
# <span data-ttu-id="1a070-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1a070-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="1a070-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a070-102">SYNOPSIS</span></span>
<span data-ttu-id="1a070-103">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1a070-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a070-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a070-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a070-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a070-105">DESCRIPTION</span></span>
<span data-ttu-id="1a070-106">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1a070-106">Create a new application insights resource</span></span>

## <span data-ttu-id="1a070-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a070-107">EXAMPLES</span></span>

### <span data-ttu-id="1a070-108">Példa 1 új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1a070-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="1a070-109">Adjon hozzá egy új, "teszt" típusú erőforrást az "testgroup" és a "Java" nevű erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="1a070-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="1a070-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a070-110">PARAMETERS</span></span>

### <span data-ttu-id="1a070-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a070-111">-Confirm</span></span>
<span data-ttu-id="1a070-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a070-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a070-113">-DefaultProfile</span></span>
<span data-ttu-id="1a070-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a070-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-115">-Kind</span><span class="sxs-lookup"><span data-stu-id="1a070-115">-Kind</span></span>
<span data-ttu-id="1a070-116">Alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="1a070-116">Application kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1a070-117">-Location</span></span>
<span data-ttu-id="1a070-118">Az alkalmazás betekintést nyújt az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="1a070-118">Application Insights Resource Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a070-119">-Name</span></span>
<span data-ttu-id="1a070-120">Az alkalmazás betekintése az erőforrás nevével</span><span class="sxs-lookup"><span data-stu-id="1a070-120">Application Insights Resource Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a070-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a070-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1a070-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="1a070-123">-Tag</span></span>
<span data-ttu-id="1a070-124">Összetevő-címkék.</span><span class="sxs-lookup"><span data-stu-id="1a070-124">Component Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a070-125">-WhatIf</span></span>
<span data-ttu-id="1a070-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a070-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a070-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a070-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a070-128">CommonParameters</span></span>
<span data-ttu-id="1a070-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a070-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a070-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a070-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a070-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a070-131">INPUTS</span></span>

### <span data-ttu-id="1a070-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a070-132">System.String</span></span>

## <span data-ttu-id="1a070-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a070-133">OUTPUTS</span></span>

### <span data-ttu-id="1a070-134">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1a070-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="1a070-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a070-135">NOTES</span></span>

## <span data-ttu-id="1a070-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a070-136">RELATED LINKS</span></span>

