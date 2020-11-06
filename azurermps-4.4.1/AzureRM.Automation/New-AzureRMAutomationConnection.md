---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497964"
---
# <span data-ttu-id="a745a-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a745a-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="a745a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a745a-102">SYNOPSIS</span></span>
<span data-ttu-id="a745a-103">Automatizálási kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a745a-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a745a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a745a-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a745a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a745a-105">DESCRIPTION</span></span>
<span data-ttu-id="a745a-106">A **New-AzureRmAutomationConnection** parancsmag létrehoz egy kapcsolatot az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a745a-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="a745a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a745a-107">EXAMPLES</span></span>

### <span data-ttu-id="a745a-108">Példa 1: kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a745a-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a745a-109">Az első parancs a mezőértékek ujjlenyomat-táblázatát rendeli a $FieldValue változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a745a-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="a745a-110">A második parancs létrehozza az Connection12 nevű Azure-kapcsolatot a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a745a-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a745a-111">A parancs a $FieldValuesban a kapcsolat mezőinek értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="a745a-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="a745a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a745a-112">PARAMETERS</span></span>

### <span data-ttu-id="a745a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a745a-113">-AutomationAccountName</span></span>
<span data-ttu-id="a745a-114">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a745a-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a745a-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="a745a-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="a745a-116">Egy kulcs/érték párokat tartalmazó kivonatoló táblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="a745a-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="a745a-117">A kulcsok a megadott kapcsolattípus kapcsolati mezőit jelzik.</span><span class="sxs-lookup"><span data-stu-id="a745a-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="a745a-118">Az értékek a csatlakozási példány egyes kapcsolat mezőinek meghatározott értékeit jelentik.</span><span class="sxs-lookup"><span data-stu-id="a745a-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a745a-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="a745a-119">-ConnectionTypeName</span></span>
<span data-ttu-id="a745a-120">A kapcsolat típusának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a745a-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a745a-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a745a-121">-Description</span></span>
<span data-ttu-id="a745a-122">A kapcsolat leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a745a-122">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a745a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a745a-123">-Name</span></span>
<span data-ttu-id="a745a-124">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a745a-124">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a745a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a745a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a745a-126">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag létrehoz egy kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="a745a-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a745a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a745a-127">-DefaultProfile</span></span>
<span data-ttu-id="a745a-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a745a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a745a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a745a-129">CommonParameters</span></span>
<span data-ttu-id="a745a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a745a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a745a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a745a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a745a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a745a-132">INPUTS</span></span>

## <span data-ttu-id="a745a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a745a-133">OUTPUTS</span></span>

### <span data-ttu-id="a745a-134">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="a745a-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a745a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a745a-135">NOTES</span></span>

## <span data-ttu-id="a745a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a745a-136">RELATED LINKS</span></span>

[<span data-ttu-id="a745a-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a745a-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="a745a-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a745a-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


