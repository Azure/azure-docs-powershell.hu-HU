---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492404"
---
# <span data-ttu-id="db753-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="db753-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="db753-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db753-102">SYNOPSIS</span></span>
<span data-ttu-id="db753-103">A DSC-vagy hibrid dolgozók bevezetéséhez szükséges regisztrációs adatok automatizálását kapja.</span><span class="sxs-lookup"><span data-stu-id="db753-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db753-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db753-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db753-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db753-105">DESCRIPTION</span></span>
<span data-ttu-id="db753-106">A **Get-AzureRmAutomationRegistrationInfo** parancsmag Kinyeri a végpontot és a szükséges kulcsokat ahhoz, hogy a kívánt állapotú (DSC) csomópontot vagy hibrid munkatársat egy Azure automatizálási fiókba lehessen beilleszteni.</span><span class="sxs-lookup"><span data-stu-id="db753-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="db753-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db753-107">EXAMPLES</span></span>

### <span data-ttu-id="db753-108">Példa 1: regisztrációs adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="db753-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="db753-109">Ez a parancs a AutomationAccount01 nevű automatizálási fiók regisztrálási adatait a ResourceGroup01 nevű Erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db753-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="db753-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db753-110">PARAMETERS</span></span>

### <span data-ttu-id="db753-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db753-111">-AutomationAccountName</span></span>
<span data-ttu-id="db753-112">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a regisztrációs adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="db753-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db753-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db753-113">-DefaultProfile</span></span>
<span data-ttu-id="db753-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="db753-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db753-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db753-115">-ResourceGroupName</span></span>
<span data-ttu-id="db753-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db753-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="db753-117">Ez a parancsmag a paraméter által megadott erőforráscsoport regisztrációs adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db753-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db753-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db753-118">CommonParameters</span></span>
<span data-ttu-id="db753-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db753-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db753-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db753-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db753-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db753-121">INPUTS</span></span>

### <span data-ttu-id="db753-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="db753-122">None</span></span>
<span data-ttu-id="db753-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="db753-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db753-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db753-124">OUTPUTS</span></span>

### <span data-ttu-id="db753-125">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="db753-125">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="db753-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db753-126">NOTES</span></span>

## <span data-ttu-id="db753-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db753-127">RELATED LINKS</span></span>

[<span data-ttu-id="db753-128">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="db753-128">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="db753-129">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="db753-129">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="db753-130">Új – AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="db753-130">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


