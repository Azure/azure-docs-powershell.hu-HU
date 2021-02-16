---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157554"
---
# <span data-ttu-id="bc666-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bc666-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="bc666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc666-102">SYNOPSIS</span></span>
<span data-ttu-id="bc666-103">Logikai alkalmazás eseményindítójának url-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="bc666-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="bc666-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc666-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc666-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc666-105">DESCRIPTION</span></span>
<span data-ttu-id="bc666-106">A **Get-Az LogicAppTriggerCallbackUrl** parancsmag egy Logic App eseményindító URL-címét kapja egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="bc666-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="bc666-107">Ez a parancsmag egy **WorkflowTriggerCallbackUrl** objektumot ad vissza, amely a visszahívási URL-címet képviseli.</span><span class="sxs-lookup"><span data-stu-id="bc666-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="bc666-108">Adja meg az erőforráscsoport nevét, a logikai alkalmazás nevét és az eseményindító nevét.</span><span class="sxs-lookup"><span data-stu-id="bc666-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="bc666-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="bc666-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bc666-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="bc666-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bc666-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="bc666-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bc666-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="bc666-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bc666-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc666-113">EXAMPLES</span></span>

### <span data-ttu-id="bc666-114">1. példa: Logikai alkalmazás eseményindítójának url-címe</span><span class="sxs-lookup"><span data-stu-id="bc666-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="bc666-115">Ez a parancs a Logic App eseményindítójának visszahívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="bc666-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="bc666-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc666-116">PARAMETERS</span></span>

### <span data-ttu-id="bc666-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc666-117">-DefaultProfile</span></span>
<span data-ttu-id="bc666-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc666-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc666-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bc666-119">-Name</span></span>
<span data-ttu-id="bc666-120">Egy logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc666-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="bc666-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc666-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc666-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc666-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bc666-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="bc666-123">-TriggerName</span></span>
<span data-ttu-id="bc666-124">Egy eseményindító nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc666-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="bc666-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc666-125">CommonParameters</span></span>
<span data-ttu-id="bc666-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc666-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc666-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc666-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc666-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc666-128">INPUTS</span></span>

### <span data-ttu-id="bc666-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bc666-129">System.String</span></span>

## <span data-ttu-id="bc666-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc666-130">OUTPUTS</span></span>

### <span data-ttu-id="bc666-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bc666-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="bc666-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc666-132">NOTES</span></span>

## <span data-ttu-id="bc666-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc666-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc666-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bc666-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


