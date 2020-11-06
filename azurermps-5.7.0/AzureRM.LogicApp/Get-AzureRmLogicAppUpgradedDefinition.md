---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: 532c0883871566326ff6ac97e891ff19755d7656
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499835"
---
# <span data-ttu-id="9b857-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="9b857-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="9b857-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b857-102">SYNOPSIS</span></span>
<span data-ttu-id="9b857-103">Egy logikai alkalmazás frissített definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b857-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b857-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b857-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b857-105">DESCRIPTION</span></span>
<span data-ttu-id="9b857-106">A **Get-AzureRmLogicAppUpgradedDefinition** parancsmag egy erőforráscsoport frissített definícióját kapja meg a séma verziószáma és a Logic App alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="9b857-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="9b857-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely a frissített logikai alkalmazás definícióját képviseli.</span><span class="sxs-lookup"><span data-stu-id="9b857-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="9b857-108">Adja meg az erőforráscsoport nevét, a Logic app nevét és a TARGET Schema verziószámát.</span><span class="sxs-lookup"><span data-stu-id="9b857-108">Specify the resource group name, logic app name, and target schema version.</span></span>

<span data-ttu-id="9b857-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9b857-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9b857-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="9b857-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9b857-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="9b857-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9b857-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="9b857-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9b857-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9b857-113">EXAMPLES</span></span>

### <span data-ttu-id="9b857-114">Példa 1: a logikai app frissített definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9b857-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="9b857-115">Az első parancs a megadott sémafájl-verzióra frissített logikai alkalmazás definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="9b857-116">A parancs a $UpgradedDefinition változóban tárolja a definíciót.</span><span class="sxs-lookup"><span data-stu-id="9b857-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>

<span data-ttu-id="9b857-117">A második parancs a $UpgradedDefinition tartalmát karakterláncként jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="9b857-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b857-118">PARAMETERS</span></span>

### <span data-ttu-id="9b857-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b857-119">-DefaultProfile</span></span>
<span data-ttu-id="9b857-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9b857-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b857-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b857-121">-Name</span></span>
<span data-ttu-id="9b857-122">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-122">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b857-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b857-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b857-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b857-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="9b857-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="9b857-126">A definíció cél-séma verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b857-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b857-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b857-127">CommonParameters</span></span>
<span data-ttu-id="9b857-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b857-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b857-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b857-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b857-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b857-130">INPUTS</span></span>

### <span data-ttu-id="9b857-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b857-131">None</span></span>
<span data-ttu-id="9b857-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9b857-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b857-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b857-133">OUTPUTS</span></span>

### <span data-ttu-id="9b857-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9b857-134">System.Object</span></span>

## <span data-ttu-id="9b857-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b857-135">NOTES</span></span>

## <span data-ttu-id="9b857-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b857-136">RELATED LINKS</span></span>

[<span data-ttu-id="9b857-137">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9b857-137">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


