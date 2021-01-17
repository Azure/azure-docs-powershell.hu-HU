---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478626"
---
# <span data-ttu-id="1c7c1-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1c7c1-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="1c7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7c1-103">Automatizálási kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="1c7c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c7c1-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c7c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1c7c1-106">A **New-AzAutomationConnection** parancsmag kapcsolatot hoz létre az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="1c7c1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c7c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1c7c1-108">1. példa: Kapcsolat létrehozása a ConnectionTypeName=Azure-hoz</span><span class="sxs-lookup"><span data-stu-id="1c7c1-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1c7c1-109">Az első parancs a mezőértékeket egy kivonatos táblához rendeli a $FieldValue változóhoz.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="1c7c1-110">A második parancs létrehoz egy Connection12 nevű Azure-kapcsolatot az AutomationAccount01 nevű Automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1c7c1-111">A parancs a kapcsolatmező-értékeket használja a $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="1c7c1-112">2. példa: Kapcsolat létrehozása a ConnectionTypeName=AzureServicePrincipal szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="1c7c1-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1c7c1-113">A parancs létrehoz egy Connection13 nevű Azure-kapcsolatot az AutomationAccount01 nevű Automatizálási fiókban az $RunAsAccountConnectionFieldValues és ConnectionTypeName=AzureServicePrincipal használatával.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="1c7c1-114">Ez a ConnectionTypeName=AzureServicePrincipal főként az Azure Run As Account szolgáltatáshoz használatos.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="1c7c1-115">3. példa: Kapcsolat létrehozása a ConnectionTypeName=AzureClassicCertificate szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="1c7c1-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1c7c1-116">A parancs létrehoz egy Connection14 nevű Azure-kapcsolatot az AutomationAccount01 nevű Automatizálási fiókban az $ClassicRunAsAccountConnectionFieldValues és ConnectionTypeName=AzureClassicCertificate használatával.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="1c7c1-117">Ez a ConnectionTypeName=AzureClassicCertificate főként az Azure Classic Run As Account szolgáltatáshoz használatos.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="1c7c1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c7c1-118">PARAMETERS</span></span>

### <span data-ttu-id="1c7c1-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c7c1-119">-AutomationAccountName</span></span>
<span data-ttu-id="1c7c1-120">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="1c7c1-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="1c7c1-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="1c7c1-122">Egy kulcs-érték párokat tartalmazó kivonattáblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="1c7c1-123">A billentyűk a megadott kapcsolattípus kapcsolatmezőit jelentik.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="1c7c1-124">Az értékek a kapcsolati példány egyes kapcsolatmezőinek konkrét értékeit jelentik.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="1c7c1-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="1c7c1-125">-ConnectionTypeName</span></span>
<span data-ttu-id="1c7c1-126">A kapcsolattípus nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="1c7c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7c1-127">-DefaultProfile</span></span>
<span data-ttu-id="1c7c1-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c7c1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c7c1-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1c7c1-129">-Description</span></span>
<span data-ttu-id="1c7c1-130">Megadja a kapcsolat leírását.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="1c7c1-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1c7c1-131">-Name</span></span>
<span data-ttu-id="1c7c1-132">Megadja a kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="1c7c1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7c1-133">-ResourceGroupName</span></span>
<span data-ttu-id="1c7c1-134">Annak az erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="1c7c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7c1-135">CommonParameters</span></span>
<span data-ttu-id="1c7c1-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7c1-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c7c1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7c1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c7c1-138">INPUTS</span></span>

### <span data-ttu-id="1c7c1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1c7c1-139">System.String</span></span>

### <span data-ttu-id="1c7c1-140">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="1c7c1-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="1c7c1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c7c1-141">OUTPUTS</span></span>

### <span data-ttu-id="1c7c1-142">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="1c7c1-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="1c7c1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c7c1-143">NOTES</span></span>

## <span data-ttu-id="1c7c1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c7c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="1c7c1-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1c7c1-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="1c7c1-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1c7c1-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


