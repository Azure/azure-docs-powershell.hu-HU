---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478774"
---
# <span data-ttu-id="e7491-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e7491-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="e7491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7491-102">SYNOPSIS</span></span>
<span data-ttu-id="e7491-103">Automatizálási fiókokat kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e7491-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="e7491-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7491-104">SYNTAX</span></span>

### <span data-ttu-id="e7491-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7491-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7491-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7491-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7491-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7491-107">DESCRIPTION</span></span>
<span data-ttu-id="e7491-108">A **Get-AzAutomationAccount** parancsmag az Azure Automation-fiókokat egy erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7491-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="e7491-109">Az automatizálási fiókokról további információt a New-AzAutomationAccount parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="e7491-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e7491-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7491-110">EXAMPLES</span></span>

### <span data-ttu-id="e7491-111">1. példa: Az összes fiók lekérte</span><span class="sxs-lookup"><span data-stu-id="e7491-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="e7491-112">Ez a parancs az Erőforráscsoport03 nevű erőforráscsoport összes automatizálási fiókját beveszi.</span><span class="sxs-lookup"><span data-stu-id="e7491-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="e7491-113">2. példa: Fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7491-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="e7491-114">Ez a parancs a ContosoAutomationAccount nevű automatizálási fiókot kapja meg a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e7491-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="e7491-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7491-115">PARAMETERS</span></span>

### <span data-ttu-id="e7491-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7491-116">-DefaultProfile</span></span>
<span data-ttu-id="e7491-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e7491-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7491-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e7491-118">-Name</span></span>
<span data-ttu-id="e7491-119">Megadja annak az automatizálási fióknak a nevét, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="e7491-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e7491-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7491-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7491-121">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="e7491-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="e7491-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7491-122">CommonParameters</span></span>
<span data-ttu-id="e7491-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7491-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7491-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7491-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7491-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7491-125">INPUTS</span></span>

### <span data-ttu-id="e7491-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e7491-126">System.String</span></span>

## <span data-ttu-id="e7491-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7491-127">OUTPUTS</span></span>

### <span data-ttu-id="e7491-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e7491-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e7491-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7491-129">NOTES</span></span>

## <span data-ttu-id="e7491-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7491-130">RELATED LINKS</span></span>

[<span data-ttu-id="e7491-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e7491-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="e7491-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e7491-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="e7491-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e7491-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


