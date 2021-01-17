---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373825"
---
# <span data-ttu-id="3c110-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="3c110-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="3c110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c110-102">SYNOPSIS</span></span>
<span data-ttu-id="3c110-103">Regisztrációs információkat kap egy DSC-csomópont vagy hibrid dolgozó automatizálásba való beírásához.</span><span class="sxs-lookup"><span data-stu-id="3c110-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="3c110-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c110-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c110-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c110-105">DESCRIPTION</span></span>
<span data-ttu-id="3c110-106">A **Get-AzAutomationRegistrationInfo** parancsmag megkapja a kívánt állapotkonfiguráció (DSC) csomópontjának vagy hibrid dolgozójának Azure Automation-fiókba való be történő bevezetőjéhez szükséges végpontot és kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="3c110-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="3c110-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c110-107">EXAMPLES</span></span>

### <span data-ttu-id="3c110-108">1. példa: Regisztrációs adatok lekérte</span><span class="sxs-lookup"><span data-stu-id="3c110-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3c110-109">Ez a parancs az AutomationAccount01 nevű Automatizálási fiók regisztrációs adatait kapja meg az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3c110-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="3c110-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c110-110">PARAMETERS</span></span>

### <span data-ttu-id="3c110-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3c110-111">-AutomationAccountName</span></span>
<span data-ttu-id="3c110-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja regisztrációs adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="3c110-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="3c110-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c110-113">-DefaultProfile</span></span>
<span data-ttu-id="3c110-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3c110-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c110-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c110-115">-ResourceGroupName</span></span>
<span data-ttu-id="3c110-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c110-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3c110-117">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c110-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c110-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c110-118">CommonParameters</span></span>
<span data-ttu-id="3c110-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c110-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c110-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c110-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c110-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c110-121">INPUTS</span></span>

### <span data-ttu-id="3c110-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3c110-122">System.String</span></span>

## <span data-ttu-id="3c110-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c110-123">OUTPUTS</span></span>

### <span data-ttu-id="3c110-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="3c110-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="3c110-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c110-125">NOTES</span></span>

## <span data-ttu-id="3c110-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c110-126">RELATED LINKS</span></span>

[<span data-ttu-id="3c110-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3c110-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="3c110-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3c110-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="3c110-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="3c110-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


