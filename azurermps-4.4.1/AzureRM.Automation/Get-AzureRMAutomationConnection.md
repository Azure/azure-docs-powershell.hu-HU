---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: e83a4c71656feb9dbe766339244e54038fa56c84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500976"
---
# <span data-ttu-id="87c4c-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="87c4c-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="87c4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="87c4c-103">Automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="87c4c-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87c4c-104">SYNTAX</span></span>

### <span data-ttu-id="87c4c-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87c4c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87c4c-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="87c4c-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87c4c-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="87c4c-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c4c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87c4c-108">DESCRIPTION</span></span>
<span data-ttu-id="87c4c-109">A **Get-AzureRmAutomationConnection** parancsmag egy vagy több Azure automatizálási kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="87c4c-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="87c4c-110">Ez a parancsmag alapértelmezés szerint beolvassa az összes kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="87c4c-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="87c4c-111">Adja meg a kapcsolat nevét egy adott kapcsolat eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="87c4c-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="87c4c-112">Adja meg a kapcsolat típusának nevét, hogy egy adott típusú kapcsolat legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="87c4c-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="87c4c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="87c4c-113">EXAMPLES</span></span>

### <span data-ttu-id="87c4c-114">Példa 1: az összes kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="87c4c-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="87c4c-115">Ez a parancs a Contoso17 nevű automatizálási fiók összes kapcsolatához metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="87c4c-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="87c4c-116">2. példa: egy típus összes kapcsolatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="87c4c-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="87c4c-117">Ez a parancs a Contoso17 nevű automatizálási fiókban a kapcsolatok metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="87c4c-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="87c4c-118">Ez a parancs a SqlServer típushoz tartozó kapcsolatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87c4c-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="87c4c-119">3. példa: kapcsolat kérése</span><span class="sxs-lookup"><span data-stu-id="87c4c-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="87c4c-120">Ez a parancs a ContosoConnection nevű kapcsolat metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="87c4c-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="87c4c-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87c4c-121">PARAMETERS</span></span>

### <span data-ttu-id="87c4c-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87c4c-122">-AutomationAccountName</span></span>
<span data-ttu-id="87c4c-123">Annak az automatizálási fióknak a neve, amelyhez a parancsmag csatlakozást kap.</span><span class="sxs-lookup"><span data-stu-id="87c4c-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="87c4c-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="87c4c-124">-ConnectionTypeName</span></span>
<span data-ttu-id="87c4c-125">Annak a kapcsolati típusnak a neve, amelyhez a parancsmag a kapcsolatokat keresi.</span><span class="sxs-lookup"><span data-stu-id="87c4c-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="87c4c-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87c4c-126">-Name</span></span>
<span data-ttu-id="87c4c-127">Annak a kapcsolatnak a nevét adja meg, amelyet a parancsmag lekérdez.</span><span class="sxs-lookup"><span data-stu-id="87c4c-127">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="87c4c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c4c-128">-ResourceGroupName</span></span>
<span data-ttu-id="87c4c-129">Annak a csoportnak a nevét adja meg, amelyhez a parancsmag csatlakozást kap.</span><span class="sxs-lookup"><span data-stu-id="87c4c-129">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="87c4c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c4c-130">-DefaultProfile</span></span>
<span data-ttu-id="87c4c-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87c4c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c4c-132">CommonParameters</span></span>
<span data-ttu-id="87c4c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87c4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c4c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c4c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c4c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87c4c-135">INPUTS</span></span>

## <span data-ttu-id="87c4c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87c4c-136">OUTPUTS</span></span>

### <span data-ttu-id="87c4c-137">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="87c4c-137">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="87c4c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87c4c-138">NOTES</span></span>

## <span data-ttu-id="87c4c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87c4c-139">RELATED LINKS</span></span>

[<span data-ttu-id="87c4c-140">Új – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="87c4c-140">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="87c4c-141">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="87c4c-141">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


