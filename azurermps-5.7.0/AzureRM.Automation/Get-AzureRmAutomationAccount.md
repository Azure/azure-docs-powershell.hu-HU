---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680832"
---
# <span data-ttu-id="d101a-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d101a-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="d101a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d101a-102">SYNOPSIS</span></span>
<span data-ttu-id="d101a-103">Automatizálási fiókokat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="d101a-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d101a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d101a-104">SYNTAX</span></span>

### <span data-ttu-id="d101a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d101a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d101a-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d101a-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d101a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d101a-107">DESCRIPTION</span></span>
<span data-ttu-id="d101a-108">A **Get-AzureRmAutomationAccount** parancsmag Azure automatizálási fiókokat kap egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="d101a-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="d101a-109">Az automatizálási fiókokról további információt az New-AzureRmAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="d101a-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="d101a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d101a-110">EXAMPLES</span></span>

### <span data-ttu-id="d101a-111">Példa 1: az összes fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="d101a-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="d101a-112">Ez a parancs a ResourceGroup03 nevű erőforráscsoport minden automatizálási fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="d101a-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="d101a-113">2. példa: fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="d101a-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="d101a-114">Ez a parancs a ContosoAutomationAccount nevű automatizálási fiókot a ContosoResourceGroup nevű erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d101a-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="d101a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d101a-115">PARAMETERS</span></span>

### <span data-ttu-id="d101a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d101a-116">-DefaultProfile</span></span>
<span data-ttu-id="d101a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d101a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d101a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d101a-118">-Name</span></span>
<span data-ttu-id="d101a-119">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d101a-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d101a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d101a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d101a-121">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="d101a-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d101a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d101a-122">CommonParameters</span></span>
<span data-ttu-id="d101a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d101a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d101a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d101a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d101a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d101a-125">INPUTS</span></span>

### <span data-ttu-id="d101a-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="d101a-126">None</span></span>
<span data-ttu-id="d101a-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d101a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d101a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d101a-128">OUTPUTS</span></span>

### <span data-ttu-id="d101a-129">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d101a-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="d101a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d101a-130">NOTES</span></span>

## <span data-ttu-id="d101a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d101a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d101a-132">Új – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d101a-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="d101a-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d101a-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="d101a-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d101a-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


