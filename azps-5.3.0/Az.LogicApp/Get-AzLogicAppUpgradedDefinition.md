---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466352"
---
# <span data-ttu-id="fab08-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="fab08-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="fab08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab08-102">SYNOPSIS</span></span>
<span data-ttu-id="fab08-103">Egy logikai alkalmazás frissített definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fab08-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="fab08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fab08-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab08-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fab08-105">DESCRIPTION</span></span>
<span data-ttu-id="fab08-106">A **Get-AzCmAppUpgradedDefinition parancsmag** egy erőforráscsoportból kapja meg a sémaverzió és a logikai alkalmazás frissített definícióját.</span><span class="sxs-lookup"><span data-stu-id="fab08-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="fab08-107">Ez a parancsmag egy objektumot ad vissza, amely a frissített logikai app definícióját képviseli.</span><span class="sxs-lookup"><span data-stu-id="fab08-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="fab08-108">Adja meg az erőforráscsoport nevét, a logikai alkalmazás nevét és a célséma verzióját.</span><span class="sxs-lookup"><span data-stu-id="fab08-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="fab08-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="fab08-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fab08-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="fab08-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fab08-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="fab08-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fab08-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="fab08-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fab08-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fab08-113">EXAMPLES</span></span>

### <span data-ttu-id="fab08-114">1. példa: A logic app frissített definíciójának lekérte</span><span class="sxs-lookup"><span data-stu-id="fab08-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="fab08-115">Az első parancs megkapja a logikai app definícióját, amely a megadott célsémára frissít.</span><span class="sxs-lookup"><span data-stu-id="fab08-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="fab08-116">A parancs a definíciót a $UpgradedDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="fab08-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="fab08-117">A második parancs karakterláncként jeleníti meg a $UpgradedDefinition tartalmát.</span><span class="sxs-lookup"><span data-stu-id="fab08-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="fab08-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab08-118">PARAMETERS</span></span>

### <span data-ttu-id="fab08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab08-119">-DefaultProfile</span></span>
<span data-ttu-id="fab08-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fab08-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fab08-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fab08-121">-Name</span></span>
<span data-ttu-id="fab08-122">Egy logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fab08-122">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab08-123">-ResourceGroupName</span></span>
<span data-ttu-id="fab08-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fab08-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fab08-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="fab08-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="fab08-126">A definíció célséma-verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fab08-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab08-127">CommonParameters</span></span>
<span data-ttu-id="fab08-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab08-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab08-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab08-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fab08-130">INPUTS</span></span>

### <span data-ttu-id="fab08-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fab08-131">System.String</span></span>

## <span data-ttu-id="fab08-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab08-132">OUTPUTS</span></span>

### <span data-ttu-id="fab08-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="fab08-133">System.Object</span></span>

## <span data-ttu-id="fab08-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fab08-134">NOTES</span></span>

## <span data-ttu-id="fab08-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fab08-135">RELATED LINKS</span></span>

[<span data-ttu-id="fab08-136">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="fab08-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


