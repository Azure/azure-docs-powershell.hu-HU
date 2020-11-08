---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195867"
---
# <span data-ttu-id="ab788-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab788-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="ab788-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab788-102">SYNOPSIS</span></span>
<span data-ttu-id="ab788-103">Logikai alkalmazást kap a visszahívás URL-címének megadásához.</span><span class="sxs-lookup"><span data-stu-id="ab788-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="ab788-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab788-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab788-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab788-105">DESCRIPTION</span></span>
<span data-ttu-id="ab788-106">A **Get-AzLogicAppTriggerCallbackUrl** parancsmag logikai alkalmazást kap, amely egy erőforráscsoport visszahívási URL-címét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ab788-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="ab788-107">Ez a parancsmag egy **WorkflowTriggerCallbackUrl** -objektumot ad eredményül, amely a visszahívás URL-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="ab788-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="ab788-108">Adja meg az erőforráscsoport nevét, a logikai app nevét és az trigger nevét.</span><span class="sxs-lookup"><span data-stu-id="ab788-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="ab788-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="ab788-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ab788-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="ab788-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ab788-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="ab788-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ab788-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="ab788-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ab788-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ab788-113">EXAMPLES</span></span>

### <span data-ttu-id="ab788-114">Példa 1: logikai app beszerzése visszahívási URL-cím</span><span class="sxs-lookup"><span data-stu-id="ab788-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="ab788-115">Ez a parancs a logikai app visszahívási URL-jét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ab788-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="ab788-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab788-116">PARAMETERS</span></span>

### <span data-ttu-id="ab788-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab788-117">-DefaultProfile</span></span>
<span data-ttu-id="ab788-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab788-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab788-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab788-119">-Name</span></span>
<span data-ttu-id="ab788-120">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab788-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab788-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab788-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab788-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab788-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab788-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ab788-123">-TriggerName</span></span>
<span data-ttu-id="ab788-124">Az indító nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab788-124">Specifies the name of a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab788-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab788-125">CommonParameters</span></span>
<span data-ttu-id="ab788-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab788-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab788-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab788-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab788-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab788-128">INPUTS</span></span>

### <span data-ttu-id="ab788-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ab788-129">System.String</span></span>

## <span data-ttu-id="ab788-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab788-130">OUTPUTS</span></span>

### <span data-ttu-id="ab788-131">Microsoft. Azure. Management. Logic. models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab788-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="ab788-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab788-132">NOTES</span></span>

## <span data-ttu-id="ab788-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab788-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab788-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab788-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

