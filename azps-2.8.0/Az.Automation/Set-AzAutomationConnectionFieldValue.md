---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 71f044dcce4944960d10fe2946b48c04354b8256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667743"
---
# <span data-ttu-id="01d17-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="01d17-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="01d17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01d17-102">SYNOPSIS</span></span>
<span data-ttu-id="01d17-103">Egy automatizálási kapcsolatban lévő mező értékének módosítása.</span><span class="sxs-lookup"><span data-stu-id="01d17-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="01d17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01d17-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01d17-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01d17-105">DESCRIPTION</span></span>
<span data-ttu-id="01d17-106">A **set-AzAutomationConnectionFieldValue** parancsmag az Azure automatizálási szolgáltatásban egy kapcsolat mezőinek értékét módosítja.</span><span class="sxs-lookup"><span data-stu-id="01d17-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="01d17-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01d17-107">EXAMPLES</span></span>

### <span data-ttu-id="01d17-108">Példa 1: mező értékének módosítása a kapcsolatokban</span><span class="sxs-lookup"><span data-stu-id="01d17-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="01d17-109">Ez a parancs a ContosoConnection nevű Azure-kapcsolat előfizetési AZONOSÍTÓját módosítja a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="01d17-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="01d17-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01d17-110">PARAMETERS</span></span>

### <span data-ttu-id="01d17-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01d17-111">-AutomationAccountName</span></span>
<span data-ttu-id="01d17-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag egy kapcsolat mezőjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="01d17-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="01d17-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="01d17-113">-ConnectionFieldName</span></span>
<span data-ttu-id="01d17-114">Annak a mezőnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="01d17-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="01d17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d17-115">-DefaultProfile</span></span>
<span data-ttu-id="01d17-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="01d17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01d17-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01d17-117">-Name</span></span>
<span data-ttu-id="01d17-118">Annak a kapcsolatnak a nevét adja meg, amelyhez ez a parancsmag módosítja a mezőt.</span><span class="sxs-lookup"><span data-stu-id="01d17-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="01d17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d17-119">-ResourceGroupName</span></span>
<span data-ttu-id="01d17-120">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy kapcsolat mezőjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="01d17-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="01d17-121">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="01d17-121">-Value</span></span>
<span data-ttu-id="01d17-122">A kapcsolat mezőben módosítani kívánt értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="01d17-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="01d17-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d17-123">CommonParameters</span></span>
<span data-ttu-id="01d17-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01d17-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d17-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d17-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d17-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d17-126">INPUTS</span></span>

### <span data-ttu-id="01d17-127">System. String</span><span class="sxs-lookup"><span data-stu-id="01d17-127">System.String</span></span>

### <span data-ttu-id="01d17-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="01d17-128">System.Object</span></span>

## <span data-ttu-id="01d17-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d17-129">OUTPUTS</span></span>

### <span data-ttu-id="01d17-130">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="01d17-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="01d17-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01d17-131">NOTES</span></span>

## <span data-ttu-id="01d17-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01d17-132">RELATED LINKS</span></span>

[<span data-ttu-id="01d17-133">Új – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01d17-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


