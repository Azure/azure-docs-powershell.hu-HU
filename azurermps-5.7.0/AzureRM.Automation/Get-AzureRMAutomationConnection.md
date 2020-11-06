---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 85d2e5d3044efe97eef2b4aa784d8767973682f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493291"
---
# <span data-ttu-id="37fe9-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="37fe9-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="37fe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="37fe9-103">Automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="37fe9-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37fe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37fe9-104">SYNTAX</span></span>

### <span data-ttu-id="37fe9-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37fe9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37fe9-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="37fe9-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37fe9-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="37fe9-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37fe9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="37fe9-108">DESCRIPTION</span></span>
<span data-ttu-id="37fe9-109">A **Get-AzureRmAutomationConnection** parancsmag egy vagy több Azure automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="37fe9-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="37fe9-110">Ez a parancsmag alapértelmezés szerint beolvassa az összes kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="37fe9-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="37fe9-111">Adja meg a kapcsolat nevét egy adott kapcsolat eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="37fe9-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="37fe9-112">Adja meg a kapcsolat típusának nevét, hogy egy adott típusú kapcsolat legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="37fe9-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="37fe9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="37fe9-113">EXAMPLES</span></span>

### <span data-ttu-id="37fe9-114">Példa 1: az összes kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="37fe9-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="37fe9-115">Ez a parancs a Contoso17 nevű automatizálási fiók összes kapcsolatához metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="37fe9-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="37fe9-116">2. példa: egy típus összes kapcsolatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="37fe9-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="37fe9-117">Ez a parancs a Contoso17 nevű automatizálási fiókban a kapcsolatok metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="37fe9-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="37fe9-118">Ez a parancs a SqlServer típushoz tartozó kapcsolatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="37fe9-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="37fe9-119">3. példa: kapcsolat kérése</span><span class="sxs-lookup"><span data-stu-id="37fe9-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="37fe9-120">Ez a parancs a ContosoConnection nevű kapcsolat metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="37fe9-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="37fe9-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37fe9-121">PARAMETERS</span></span>

### <span data-ttu-id="37fe9-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37fe9-122">-AutomationAccountName</span></span>
<span data-ttu-id="37fe9-123">Annak az automatizálási fióknak a neve, amelyhez a parancsmag csatlakozást kap.</span><span class="sxs-lookup"><span data-stu-id="37fe9-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="37fe9-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="37fe9-124">-ConnectionTypeName</span></span>
<span data-ttu-id="37fe9-125">Annak a kapcsolati típusnak a neve, amelyhez a parancsmag a kapcsolatokat keresi.</span><span class="sxs-lookup"><span data-stu-id="37fe9-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fe9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fe9-126">-DefaultProfile</span></span>
<span data-ttu-id="37fe9-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37fe9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37fe9-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37fe9-128">-Name</span></span>
<span data-ttu-id="37fe9-129">Annak a kapcsolatnak a nevét adja meg, amelyet a parancsmag lekérdez.</span><span class="sxs-lookup"><span data-stu-id="37fe9-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fe9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fe9-130">-ResourceGroupName</span></span>
<span data-ttu-id="37fe9-131">Annak a csoportnak a nevét adja meg, amelyhez a parancsmag csatlakozást kap.</span><span class="sxs-lookup"><span data-stu-id="37fe9-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="37fe9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fe9-132">CommonParameters</span></span>
<span data-ttu-id="37fe9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37fe9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fe9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37fe9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fe9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37fe9-135">INPUTS</span></span>

### <span data-ttu-id="37fe9-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="37fe9-136">None</span></span>
<span data-ttu-id="37fe9-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="37fe9-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37fe9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37fe9-138">OUTPUTS</span></span>

### <span data-ttu-id="37fe9-139">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="37fe9-139">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="37fe9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37fe9-140">NOTES</span></span>

## <span data-ttu-id="37fe9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37fe9-141">RELATED LINKS</span></span>

[<span data-ttu-id="37fe9-142">Új – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="37fe9-142">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="37fe9-143">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="37fe9-143">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


