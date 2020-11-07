---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 80e322fe589fbfe8d13ab9a754c98bec2fff741f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835466"
---
# <span data-ttu-id="5f5da-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="5f5da-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="5f5da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f5da-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5da-103">Egy logikai alkalmazás frissített definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="5f5da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f5da-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f5da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f5da-105">DESCRIPTION</span></span>
<span data-ttu-id="5f5da-106">A **Get-AzLogicAppUpgradedDefinition** parancsmag egy erőforráscsoport frissített definícióját kapja meg a séma verziószáma és a Logic App alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="5f5da-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="5f5da-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely a frissített logikai alkalmazás definícióját képviseli.</span><span class="sxs-lookup"><span data-stu-id="5f5da-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="5f5da-108">Adja meg az erőforráscsoport nevét, a Logic app nevét és a TARGET Schema verziószámát.</span><span class="sxs-lookup"><span data-stu-id="5f5da-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="5f5da-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5f5da-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5f5da-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="5f5da-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5f5da-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="5f5da-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5f5da-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="5f5da-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5f5da-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5f5da-113">EXAMPLES</span></span>

### <span data-ttu-id="5f5da-114">Példa 1: a logikai app frissített definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5f5da-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="5f5da-115">Az első parancs a megadott sémafájl-verzióra frissített logikai alkalmazás definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="5f5da-116">A parancs a $UpgradedDefinition változóban tárolja a definíciót.</span><span class="sxs-lookup"><span data-stu-id="5f5da-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="5f5da-117">A második parancs a $UpgradedDefinition tartalmát karakterláncként jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="5f5da-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f5da-118">PARAMETERS</span></span>

### <span data-ttu-id="5f5da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5da-119">-DefaultProfile</span></span>
<span data-ttu-id="5f5da-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5f5da-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f5da-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f5da-121">-Name</span></span>
<span data-ttu-id="5f5da-122">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="5f5da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f5da-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f5da-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5f5da-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="5f5da-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="5f5da-126">A definíció cél-séma verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f5da-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="5f5da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5da-127">CommonParameters</span></span>
<span data-ttu-id="5f5da-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f5da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5da-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5da-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5da-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f5da-130">INPUTS</span></span>

### <span data-ttu-id="5f5da-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f5da-131">System.String</span></span>

## <span data-ttu-id="5f5da-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f5da-132">OUTPUTS</span></span>

### <span data-ttu-id="5f5da-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5f5da-133">System.Object</span></span>

## <span data-ttu-id="5f5da-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f5da-134">NOTES</span></span>

## <span data-ttu-id="5f5da-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f5da-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f5da-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="5f5da-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


