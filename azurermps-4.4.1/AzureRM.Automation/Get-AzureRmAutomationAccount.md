---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: d79f46e645bb5889c58aaca4b3fbdd046be5c756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679119"
---
# <span data-ttu-id="add68-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add68-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="add68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="add68-102">SYNOPSIS</span></span>
<span data-ttu-id="add68-103">Automatizálási fiókokat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="add68-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="add68-104">SYNTAX</span></span>

### <span data-ttu-id="add68-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="add68-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="add68-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="add68-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add68-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="add68-107">DESCRIPTION</span></span>
<span data-ttu-id="add68-108">A **Get-AzureRmAutomationAccount** parancsmag Azure automatizálási fiókokat kap egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="add68-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="add68-109">Az automatizálási fiókokról további információt az New-AzureRmAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="add68-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="add68-110">Példák</span><span class="sxs-lookup"><span data-stu-id="add68-110">EXAMPLES</span></span>

### <span data-ttu-id="add68-111">Példa 1: az összes fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="add68-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="add68-112">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden automatizálási fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="add68-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="add68-113">2. példa: fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="add68-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="add68-114">Ez a parancs a ContosoAutomationAccount nevű automatizálási fiókot a ContosoResourceGroup nevű erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="add68-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="add68-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="add68-115">PARAMETERS</span></span>

### <span data-ttu-id="add68-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="add68-116">-Name</span></span>
<span data-ttu-id="add68-117">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="add68-117">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="add68-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add68-118">-ResourceGroupName</span></span>
<span data-ttu-id="add68-119">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="add68-119">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="add68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add68-120">-DefaultProfile</span></span>
<span data-ttu-id="add68-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="add68-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add68-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add68-122">CommonParameters</span></span>
<span data-ttu-id="add68-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="add68-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add68-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add68-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add68-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="add68-125">INPUTS</span></span>

## <span data-ttu-id="add68-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="add68-126">OUTPUTS</span></span>

### <span data-ttu-id="add68-127">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add68-127">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="add68-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="add68-128">NOTES</span></span>

## <span data-ttu-id="add68-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="add68-129">RELATED LINKS</span></span>

[<span data-ttu-id="add68-130">Új – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add68-130">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="add68-131">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add68-131">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="add68-132">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add68-132">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


