---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: aaa4a87f14572650fb0c1f969c11f0a3ed9cf0e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014294"
---
# <span data-ttu-id="2be96-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="2be96-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="2be96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be96-102">SYNOPSIS</span></span>
<span data-ttu-id="2be96-103">Regisztrációs információkat kap egy DSC-csomópont vagy hibrid dolgozó automatizálásba való beírásához.</span><span class="sxs-lookup"><span data-stu-id="2be96-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="2be96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2be96-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2be96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2be96-105">DESCRIPTION</span></span>
<span data-ttu-id="2be96-106">A **Get-AzAutomationRegistrationInfo** parancsmag megkapja a kívánt állapotkonfiguráció (DSC) csomópontjának vagy hibrid dolgozójának Azure Automation-fiókba való be történő bevezetőjéhez szükséges végpontot és kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="2be96-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="2be96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2be96-107">EXAMPLES</span></span>

### <span data-ttu-id="2be96-108">1. példa: Regisztrációs adatok lekérte</span><span class="sxs-lookup"><span data-stu-id="2be96-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2be96-109">Ez a parancs az AutomationAccount01 nevű Automatizálási fiók regisztrációs adatait kapja az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="2be96-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="2be96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2be96-110">PARAMETERS</span></span>

### <span data-ttu-id="2be96-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2be96-111">-AutomationAccountName</span></span>
<span data-ttu-id="2be96-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja regisztrációs adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="2be96-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="2be96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be96-113">-DefaultProfile</span></span>
<span data-ttu-id="2be96-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2be96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2be96-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be96-115">-ResourceGroupName</span></span>
<span data-ttu-id="2be96-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2be96-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2be96-117">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2be96-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2be96-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be96-118">CommonParameters</span></span>
<span data-ttu-id="2be96-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be96-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be96-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be96-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be96-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2be96-121">INPUTS</span></span>

### <span data-ttu-id="2be96-122">System.String</span><span class="sxs-lookup"><span data-stu-id="2be96-122">System.String</span></span>

## <span data-ttu-id="2be96-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2be96-123">OUTPUTS</span></span>

### <span data-ttu-id="2be96-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="2be96-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="2be96-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2be96-125">NOTES</span></span>

## <span data-ttu-id="2be96-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2be96-126">RELATED LINKS</span></span>

[<span data-ttu-id="2be96-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2be96-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="2be96-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2be96-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="2be96-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="2be96-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


