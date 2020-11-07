---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671573"
---
# <span data-ttu-id="4187c-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4187c-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="4187c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4187c-102">SYNOPSIS</span></span>
<span data-ttu-id="4187c-103">Automatizálási kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4187c-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="4187c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4187c-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4187c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4187c-105">DESCRIPTION</span></span>
<span data-ttu-id="4187c-106">A **New-AzAutomationConnection** parancsmag létrehoz egy kapcsolatot az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="4187c-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="4187c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4187c-107">EXAMPLES</span></span>

### <span data-ttu-id="4187c-108">Példa 1: kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="4187c-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4187c-109">Az első parancs a mezőértékek ujjlenyomat-táblázatát rendeli a $FieldValue változóhoz.</span><span class="sxs-lookup"><span data-stu-id="4187c-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="4187c-110">A második parancs létrehozza az Connection12 nevű Azure-kapcsolatot a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="4187c-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4187c-111">A parancs a $FieldValuesban a kapcsolat mezőinek értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="4187c-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="4187c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4187c-112">PARAMETERS</span></span>

### <span data-ttu-id="4187c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4187c-113">-AutomationAccountName</span></span>
<span data-ttu-id="4187c-114">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4187c-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4187c-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="4187c-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="4187c-116">Egy kulcs/érték párokat tartalmazó kivonatoló táblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="4187c-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="4187c-117">A kulcsok a megadott kapcsolattípus kapcsolati mezőit jelzik.</span><span class="sxs-lookup"><span data-stu-id="4187c-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="4187c-118">Az értékek a csatlakozási példány egyes kapcsolat mezőinek meghatározott értékeit jelentik.</span><span class="sxs-lookup"><span data-stu-id="4187c-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="4187c-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4187c-119">-ConnectionTypeName</span></span>
<span data-ttu-id="4187c-120">A kapcsolat típusának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4187c-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="4187c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4187c-121">-DefaultProfile</span></span>
<span data-ttu-id="4187c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4187c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4187c-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4187c-123">-Description</span></span>
<span data-ttu-id="4187c-124">A kapcsolat leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4187c-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="4187c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4187c-125">-Name</span></span>
<span data-ttu-id="4187c-126">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4187c-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="4187c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4187c-127">-ResourceGroupName</span></span>
<span data-ttu-id="4187c-128">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag létrehoz egy kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4187c-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4187c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4187c-129">CommonParameters</span></span>
<span data-ttu-id="4187c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4187c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4187c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4187c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4187c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4187c-132">INPUTS</span></span>

### <span data-ttu-id="4187c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4187c-133">System.String</span></span>

### <span data-ttu-id="4187c-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4187c-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="4187c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4187c-135">OUTPUTS</span></span>

### <span data-ttu-id="4187c-136">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="4187c-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4187c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4187c-137">NOTES</span></span>

## <span data-ttu-id="4187c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4187c-138">RELATED LINKS</span></span>

[<span data-ttu-id="4187c-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4187c-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="4187c-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4187c-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


