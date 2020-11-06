---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497976"
---
# <span data-ttu-id="2a213-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="2a213-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="2a213-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a213-102">SYNOPSIS</span></span>
<span data-ttu-id="2a213-103">A DSC-vagy hibrid dolgozók bevezetéséhez szükséges regisztrációs adatok automatizálását kapja.</span><span class="sxs-lookup"><span data-stu-id="2a213-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a213-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a213-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a213-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a213-105">DESCRIPTION</span></span>
<span data-ttu-id="2a213-106">A **Get-AzureRmAutomationRegistrationInfo** parancsmag Kinyeri a végpontot és a szükséges kulcsokat ahhoz, hogy a kívánt állapotú (DSC) csomópontot vagy hibrid munkatársat egy Azure automatizálási fiókba lehessen beilleszteni.</span><span class="sxs-lookup"><span data-stu-id="2a213-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="2a213-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2a213-107">EXAMPLES</span></span>

### <span data-ttu-id="2a213-108">Példa 1: regisztrációs adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a213-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2a213-109">Ez a parancs a AutomationAccount01 nevű automatizálási fiók regisztrálási adatait a ResourceGroup01 nevű Erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2a213-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="2a213-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a213-110">PARAMETERS</span></span>

### <span data-ttu-id="2a213-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2a213-111">-AutomationAccountName</span></span>
<span data-ttu-id="2a213-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a regisztrációs adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="2a213-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="2a213-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a213-113">-ResourceGroupName</span></span>
<span data-ttu-id="2a213-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a213-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2a213-115">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2a213-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a213-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a213-116">-DefaultProfile</span></span>
<span data-ttu-id="2a213-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a213-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a213-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a213-118">CommonParameters</span></span>
<span data-ttu-id="2a213-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a213-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a213-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a213-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a213-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a213-121">INPUTS</span></span>

## <span data-ttu-id="2a213-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a213-122">OUTPUTS</span></span>

### <span data-ttu-id="2a213-123">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="2a213-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="2a213-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a213-124">NOTES</span></span>

## <span data-ttu-id="2a213-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a213-125">RELATED LINKS</span></span>

[<span data-ttu-id="2a213-126">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a213-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="2a213-127">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2a213-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="2a213-128">Új – AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="2a213-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


