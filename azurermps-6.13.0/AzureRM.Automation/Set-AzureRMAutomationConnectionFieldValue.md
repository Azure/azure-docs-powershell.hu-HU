---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: fa5faafe9a7d0b7c27e5bb596e56bfadf88e5608
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679190"
---
# <span data-ttu-id="9f299-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9f299-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="9f299-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f299-102">SYNOPSIS</span></span>
<span data-ttu-id="9f299-103">Egy automatizálási kapcsolatban lévő mező értékének módosítása.</span><span class="sxs-lookup"><span data-stu-id="9f299-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f299-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f299-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f299-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f299-105">DESCRIPTION</span></span>
<span data-ttu-id="9f299-106">A **set-AzureRmAutomationConnectionFieldValue** parancsmag az Azure automatizálási szolgáltatásban egy kapcsolat mezőinek értékét módosítja.</span><span class="sxs-lookup"><span data-stu-id="9f299-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="9f299-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9f299-107">EXAMPLES</span></span>

### <span data-ttu-id="9f299-108">Példa 1: mező értékének módosítása a kapcsolatokban</span><span class="sxs-lookup"><span data-stu-id="9f299-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9f299-109">Ez a parancs a ContosoConnection nevű Azure-kapcsolat előfizetési AZONOSÍTÓját módosítja a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9f299-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="9f299-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f299-110">PARAMETERS</span></span>

### <span data-ttu-id="9f299-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f299-111">-AutomationAccountName</span></span>
<span data-ttu-id="9f299-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag egy kapcsolat mezőjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="9f299-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="9f299-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="9f299-113">-ConnectionFieldName</span></span>
<span data-ttu-id="9f299-114">Annak a mezőnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="9f299-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9f299-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f299-115">-DefaultProfile</span></span>
<span data-ttu-id="9f299-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f299-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f299-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f299-117">-Name</span></span>
<span data-ttu-id="9f299-118">Annak a kapcsolatnak a nevét adja meg, amelyhez ez a parancsmag módosítja a mezőt.</span><span class="sxs-lookup"><span data-stu-id="9f299-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="9f299-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f299-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f299-120">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy kapcsolat mezőjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="9f299-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="9f299-121">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="9f299-121">-Value</span></span>
<span data-ttu-id="9f299-122">A kapcsolat mezőben módosítani kívánt értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f299-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="9f299-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f299-123">CommonParameters</span></span>
<span data-ttu-id="9f299-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f299-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f299-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f299-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f299-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f299-126">INPUTS</span></span>

### <span data-ttu-id="9f299-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9f299-127">System.String</span></span>

### <span data-ttu-id="9f299-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9f299-128">System.Object</span></span>

## <span data-ttu-id="9f299-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f299-129">OUTPUTS</span></span>

### <span data-ttu-id="9f299-130">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9f299-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9f299-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f299-131">NOTES</span></span>

## <span data-ttu-id="9f299-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f299-132">RELATED LINKS</span></span>

[<span data-ttu-id="9f299-133">Új – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9f299-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


