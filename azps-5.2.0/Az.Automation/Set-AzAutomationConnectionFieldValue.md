---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373111"
---
# <span data-ttu-id="fc8b4-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="fc8b4-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="fc8b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8b4-103">Módosítja egy automatizálási kapcsolat egyik mezőjének értékét.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="fc8b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc8b4-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc8b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc8b4-106">A **Set-AzAutomationConnectionFieldValue** parancsmag módosítja egy kapcsolat egy mezőjének értékét az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="fc8b4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc8b4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc8b4-108">1. példa: Kapcsolat mezőértékének módosítása</span><span class="sxs-lookup"><span data-stu-id="fc8b4-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="fc8b4-109">Ez a parancs módosítja a ContosoConnection nevű Azure-kapcsolat előfizetésazonosítóját az AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="fc8b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc8b4-110">PARAMETERS</span></span>

### <span data-ttu-id="fc8b4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc8b4-111">-AutomationAccountName</span></span>
<span data-ttu-id="fc8b4-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja módosítja egy kapcsolat egyik mezőjét.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b4-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="fc8b4-113">-ConnectionFieldName</span></span>
<span data-ttu-id="fc8b4-114">Megadja annak a mezőnek a nevét, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fc8b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8b4-115">-DefaultProfile</span></span>
<span data-ttu-id="fc8b4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fc8b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc8b4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fc8b4-117">-Name</span></span>
<span data-ttu-id="fc8b4-118">Annak a kapcsolatnak a nevét adja meg, amelynek a parancsmagja módosít egy mezőt.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc8b4-120">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja módosítja egy kapcsolat egyik mezőjét.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b4-121">-Érték</span><span class="sxs-lookup"><span data-stu-id="fc8b4-121">-Value</span></span>
<span data-ttu-id="fc8b4-122">A kapcsolatmezőben módosíthat egy értéket.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8b4-123">CommonParameters</span></span>
<span data-ttu-id="fc8b4-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8b4-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8b4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8b4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc8b4-126">INPUTS</span></span>

### <span data-ttu-id="fc8b4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fc8b4-127">System.String</span></span>

### <span data-ttu-id="fc8b4-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="fc8b4-128">System.Object</span></span>

## <span data-ttu-id="fc8b4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc8b4-129">OUTPUTS</span></span>

### <span data-ttu-id="fc8b4-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="fc8b4-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="fc8b4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc8b4-131">NOTES</span></span>

## <span data-ttu-id="fc8b4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc8b4-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc8b4-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="fc8b4-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


