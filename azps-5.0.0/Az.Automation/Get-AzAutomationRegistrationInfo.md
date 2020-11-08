---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188136"
---
# <span data-ttu-id="9eeba-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="9eeba-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="9eeba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9eeba-102">SYNOPSIS</span></span>
<span data-ttu-id="9eeba-103">A DSC-vagy hibrid dolgozók bevezetéséhez szükséges regisztrációs adatok automatizálását kapja.</span><span class="sxs-lookup"><span data-stu-id="9eeba-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="9eeba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9eeba-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eeba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9eeba-105">DESCRIPTION</span></span>
<span data-ttu-id="9eeba-106">A **Get-AzAutomationRegistrationInfo** parancsmag Kinyeri a végpontot és a szükséges kulcsokat ahhoz, hogy a kívánt állapotú (DSC) csomópontot vagy hibrid munkatársat egy Azure automatizálási fiókba lehessen beilleszteni.</span><span class="sxs-lookup"><span data-stu-id="9eeba-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="9eeba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9eeba-107">EXAMPLES</span></span>

### <span data-ttu-id="9eeba-108">Példa 1: regisztrációs adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="9eeba-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9eeba-109">Ez a parancs a AutomationAccount01 nevű automatizálási fiók regisztrálási adatait a ResourceGroup01 nevű Erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eeba-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="9eeba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9eeba-110">PARAMETERS</span></span>

### <span data-ttu-id="9eeba-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9eeba-111">-AutomationAccountName</span></span>
<span data-ttu-id="9eeba-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a regisztrációs adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="9eeba-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="9eeba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eeba-113">-DefaultProfile</span></span>
<span data-ttu-id="9eeba-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9eeba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eeba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eeba-115">-ResourceGroupName</span></span>
<span data-ttu-id="9eeba-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9eeba-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9eeba-117">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eeba-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9eeba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eeba-118">CommonParameters</span></span>
<span data-ttu-id="9eeba-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9eeba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eeba-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eeba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eeba-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eeba-121">INPUTS</span></span>

### <span data-ttu-id="9eeba-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9eeba-122">System.String</span></span>

## <span data-ttu-id="9eeba-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eeba-123">OUTPUTS</span></span>

### <span data-ttu-id="9eeba-124">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="9eeba-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="9eeba-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9eeba-125">NOTES</span></span>

## <span data-ttu-id="9eeba-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eeba-126">RELATED LINKS</span></span>

[<span data-ttu-id="9eeba-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9eeba-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="9eeba-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9eeba-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="9eeba-129">Új – AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="9eeba-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)

