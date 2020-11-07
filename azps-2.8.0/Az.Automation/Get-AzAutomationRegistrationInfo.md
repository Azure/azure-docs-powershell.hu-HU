---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: f915d1637226e7381cf7da53c0a3aea022060be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667839"
---
# <span data-ttu-id="01d23-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="01d23-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="01d23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01d23-102">SYNOPSIS</span></span>
<span data-ttu-id="01d23-103">A DSC-vagy hibrid dolgozók bevezetéséhez szükséges regisztrációs adatok automatizálását kapja.</span><span class="sxs-lookup"><span data-stu-id="01d23-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="01d23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01d23-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d23-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01d23-105">DESCRIPTION</span></span>
<span data-ttu-id="01d23-106">A **Get-AzAutomationRegistrationInfo** parancsmag Kinyeri a végpontot és a szükséges kulcsokat ahhoz, hogy a kívánt állapotú (DSC) csomópontot vagy hibrid munkatársat egy Azure automatizálási fiókba lehessen beilleszteni.</span><span class="sxs-lookup"><span data-stu-id="01d23-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="01d23-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01d23-107">EXAMPLES</span></span>

### <span data-ttu-id="01d23-108">Példa 1: regisztrációs adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="01d23-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="01d23-109">Ez a parancs a AutomationAccount01 nevű automatizálási fiók regisztrálási adatait a ResourceGroup01 nevű Erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01d23-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="01d23-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01d23-110">PARAMETERS</span></span>

### <span data-ttu-id="01d23-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01d23-111">-AutomationAccountName</span></span>
<span data-ttu-id="01d23-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a regisztrációs adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="01d23-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="01d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d23-113">-DefaultProfile</span></span>
<span data-ttu-id="01d23-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="01d23-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01d23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d23-115">-ResourceGroupName</span></span>
<span data-ttu-id="01d23-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01d23-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="01d23-117">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01d23-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="01d23-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d23-118">CommonParameters</span></span>
<span data-ttu-id="01d23-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01d23-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d23-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d23-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d23-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d23-121">INPUTS</span></span>

### <span data-ttu-id="01d23-122">System. String</span><span class="sxs-lookup"><span data-stu-id="01d23-122">System.String</span></span>

## <span data-ttu-id="01d23-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d23-123">OUTPUTS</span></span>

### <span data-ttu-id="01d23-124">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="01d23-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="01d23-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01d23-125">NOTES</span></span>

## <span data-ttu-id="01d23-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01d23-126">RELATED LINKS</span></span>

[<span data-ttu-id="01d23-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="01d23-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="01d23-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="01d23-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="01d23-129">Új – AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="01d23-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


