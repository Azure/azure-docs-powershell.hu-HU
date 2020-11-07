---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 6c5e0a376b8170c73abc394f275995b178e90917
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671643"
---
# <span data-ttu-id="ebddb-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ebddb-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="ebddb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebddb-102">SYNOPSIS</span></span>
<span data-ttu-id="ebddb-103">Automatizálási fiókokat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="ebddb-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="ebddb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebddb-104">SYNTAX</span></span>

### <span data-ttu-id="ebddb-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebddb-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebddb-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ebddb-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebddb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebddb-107">DESCRIPTION</span></span>
<span data-ttu-id="ebddb-108">A **Get-AzAutomationAccount** parancsmag Azure automatizálási fiókokat kap egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="ebddb-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="ebddb-109">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ebddb-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ebddb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ebddb-110">EXAMPLES</span></span>

### <span data-ttu-id="ebddb-111">Példa 1: az összes fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="ebddb-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="ebddb-112">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden automatizálási fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="ebddb-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="ebddb-113">2. példa: fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="ebddb-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="ebddb-114">Ez a parancs a ContosoAutomationAccount nevű automatizálási fiókot a ContosoResourceGroup nevű erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ebddb-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="ebddb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebddb-115">PARAMETERS</span></span>

### <span data-ttu-id="ebddb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebddb-116">-DefaultProfile</span></span>
<span data-ttu-id="ebddb-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebddb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebddb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebddb-118">-Name</span></span>
<span data-ttu-id="ebddb-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ebddb-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ebddb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebddb-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebddb-121">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="ebddb-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="ebddb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebddb-122">CommonParameters</span></span>
<span data-ttu-id="ebddb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebddb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebddb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebddb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebddb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebddb-125">INPUTS</span></span>

### <span data-ttu-id="ebddb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ebddb-126">System.String</span></span>

## <span data-ttu-id="ebddb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebddb-127">OUTPUTS</span></span>

### <span data-ttu-id="ebddb-128">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ebddb-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ebddb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebddb-129">NOTES</span></span>

## <span data-ttu-id="ebddb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebddb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebddb-131">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ebddb-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ebddb-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ebddb-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="ebddb-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ebddb-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


