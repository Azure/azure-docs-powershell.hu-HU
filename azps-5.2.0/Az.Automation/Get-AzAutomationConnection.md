---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328407"
---
# <span data-ttu-id="d8486-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8486-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="d8486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8486-102">SYNOPSIS</span></span>
<span data-ttu-id="d8486-103">Automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="d8486-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="d8486-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8486-104">SYNTAX</span></span>

### <span data-ttu-id="d8486-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8486-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8486-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="d8486-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8486-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="d8486-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8486-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8486-108">DESCRIPTION</span></span>
<span data-ttu-id="d8486-109">A **Get-AzAutomationConnection** parancsmag egy vagy több Azure Automation-kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="d8486-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="d8486-110">Ez a parancsmag alapértelmezés szerint beolvassa az összes kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="d8486-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="d8486-111">Adja meg a kapcsolat nevét, ha adott kapcsolatot létesít.</span><span class="sxs-lookup"><span data-stu-id="d8486-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="d8486-112">Adja meg a kapcsolattípus nevét egy adott típusú kapcsolat be szereznie.</span><span class="sxs-lookup"><span data-stu-id="d8486-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="d8486-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8486-113">EXAMPLES</span></span>

### <span data-ttu-id="d8486-114">1. példa: Az összes kapcsolat lekérte</span><span class="sxs-lookup"><span data-stu-id="d8486-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d8486-115">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes kapcsolatához.</span><span class="sxs-lookup"><span data-stu-id="d8486-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d8486-116">2. példa: Az összes kapcsolat be szerezni egy típust</span><span class="sxs-lookup"><span data-stu-id="d8486-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="d8486-117">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiókban található kapcsolatokhoz.</span><span class="sxs-lookup"><span data-stu-id="d8486-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="d8486-118">Ez a parancs SqlServer típusú kapcsolatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d8486-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="d8486-119">3. példa: Kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8486-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="d8486-120">Ez a parancs a ContosoConnection nevű kapcsolat metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d8486-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="d8486-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8486-121">PARAMETERS</span></span>

### <span data-ttu-id="d8486-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8486-122">-AutomationAccountName</span></span>
<span data-ttu-id="d8486-123">Annak az automatizálási fióknak a nevét adja meg, amelyhez a parancsmag kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="d8486-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="d8486-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="d8486-124">-ConnectionTypeName</span></span>
<span data-ttu-id="d8486-125">Annak a kapcsolattípusnak a nevét adja meg, amelyhez a parancsmag beolvassa a kapcsolatokat.</span><span class="sxs-lookup"><span data-stu-id="d8486-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8486-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8486-126">-DefaultProfile</span></span>
<span data-ttu-id="d8486-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8486-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8486-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d8486-128">-Name</span></span>
<span data-ttu-id="d8486-129">A parancsmag által lekért kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8486-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8486-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8486-130">-ResourceGroupName</span></span>
<span data-ttu-id="d8486-131">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a parancsmag kapcsolatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d8486-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="d8486-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8486-132">CommonParameters</span></span>
<span data-ttu-id="d8486-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8486-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8486-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8486-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8486-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8486-135">INPUTS</span></span>

### <span data-ttu-id="d8486-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d8486-136">System.String</span></span>

## <span data-ttu-id="d8486-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8486-137">OUTPUTS</span></span>

### <span data-ttu-id="d8486-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="d8486-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="d8486-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8486-139">NOTES</span></span>

## <span data-ttu-id="d8486-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8486-140">RELATED LINKS</span></span>

[<span data-ttu-id="d8486-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8486-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="d8486-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8486-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


