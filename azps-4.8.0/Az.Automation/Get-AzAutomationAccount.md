---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024932"
---
# <span data-ttu-id="b2291-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2291-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="b2291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2291-102">SYNOPSIS</span></span>
<span data-ttu-id="b2291-103">Automatizálási fiókokat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="b2291-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="b2291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2291-104">SYNTAX</span></span>

### <span data-ttu-id="b2291-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2291-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2291-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2291-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2291-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2291-107">DESCRIPTION</span></span>
<span data-ttu-id="b2291-108">A **Get-AzAutomationAccount** parancsmag Azure automatizálási fiókokat kap egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="b2291-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="b2291-109">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="b2291-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="b2291-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b2291-110">EXAMPLES</span></span>

### <span data-ttu-id="b2291-111">Példa 1: az összes fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="b2291-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="b2291-112">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden automatizálási fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="b2291-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="b2291-113">2. példa: fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="b2291-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="b2291-114">Ez a parancs a ContosoAutomationAccount nevű automatizálási fiókot a ContosoResourceGroup nevű erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2291-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="b2291-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2291-115">PARAMETERS</span></span>

### <span data-ttu-id="b2291-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2291-116">-DefaultProfile</span></span>
<span data-ttu-id="b2291-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2291-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2291-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2291-118">-Name</span></span>
<span data-ttu-id="b2291-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b2291-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2291-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2291-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2291-121">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="b2291-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2291-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2291-122">CommonParameters</span></span>
<span data-ttu-id="b2291-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2291-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2291-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2291-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2291-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2291-125">INPUTS</span></span>

### <span data-ttu-id="b2291-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b2291-126">System.String</span></span>

## <span data-ttu-id="b2291-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2291-127">OUTPUTS</span></span>

### <span data-ttu-id="b2291-128">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2291-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="b2291-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2291-129">NOTES</span></span>

## <span data-ttu-id="b2291-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2291-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2291-131">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2291-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="b2291-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2291-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="b2291-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2291-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


