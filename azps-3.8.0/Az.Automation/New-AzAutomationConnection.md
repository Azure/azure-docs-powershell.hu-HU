---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014973"
---
# <span data-ttu-id="9938b-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9938b-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="9938b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9938b-102">SYNOPSIS</span></span>
<span data-ttu-id="9938b-103">Automatizálási kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9938b-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="9938b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9938b-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9938b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9938b-105">DESCRIPTION</span></span>
<span data-ttu-id="9938b-106">A **New-AzAutomationConnection** parancsmag létrehoz egy kapcsolatot az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="9938b-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="9938b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9938b-107">EXAMPLES</span></span>

### <span data-ttu-id="9938b-108">Példa 1: kapcsolat létrehozása a ConnectionTypeName = Azure</span><span class="sxs-lookup"><span data-stu-id="9938b-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9938b-109">Az első parancs a mezőértékek ujjlenyomat-táblázatát rendeli a $FieldValue változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9938b-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="9938b-110">A második parancs létrehozza az Connection12 nevű Azure-kapcsolatot a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9938b-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="9938b-111">A parancs a $FieldValuesban a kapcsolat mezőinek értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="9938b-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="9938b-112">2. példa: kapcsolat létrehozása a ConnectionTypeName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9938b-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9938b-113">A parancs létrehoz egy Connection13 nevű Azure-kapcsolatot a AutomationAccount01 nevű automatizálási fiókban $RunAsAccountConnectionFieldValues és ConnectionTypeName = AzureServicePrincipal segítségével.</span><span class="sxs-lookup"><span data-stu-id="9938b-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="9938b-114">Ezt a ConnectionTypeName = AzureServicePrincipal-ot főleg az Azure Run fiókként használja.</span><span class="sxs-lookup"><span data-stu-id="9938b-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="9938b-115">3. példa: kapcsolat létrehozása a ConnectionTypeName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="9938b-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9938b-116">A parancs létrehoz egy Connection14 nevű Azure-kapcsolatot a AutomationAccount01 nevű automatizálási fiókban $ClassicRunAsAccountConnectionFieldValues és ConnectionTypeName = AzureClassicCertificate segítségével.</span><span class="sxs-lookup"><span data-stu-id="9938b-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="9938b-117">Ez a ConnectionTypeName = AzureClassicCertificate főként az Azure Classic Run as fiókként használható.</span><span class="sxs-lookup"><span data-stu-id="9938b-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="9938b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9938b-118">PARAMETERS</span></span>

### <span data-ttu-id="9938b-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9938b-119">-AutomationAccountName</span></span>
<span data-ttu-id="9938b-120">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9938b-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="9938b-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="9938b-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="9938b-122">Egy kulcs/érték párokat tartalmazó kivonatoló táblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="9938b-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="9938b-123">A kulcsok a megadott kapcsolattípus kapcsolati mezőit jelzik.</span><span class="sxs-lookup"><span data-stu-id="9938b-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="9938b-124">Az értékek a csatlakozási példány egyes kapcsolat mezőinek meghatározott értékeit jelentik.</span><span class="sxs-lookup"><span data-stu-id="9938b-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="9938b-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9938b-125">-ConnectionTypeName</span></span>
<span data-ttu-id="9938b-126">A kapcsolat típusának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9938b-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="9938b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9938b-127">-DefaultProfile</span></span>
<span data-ttu-id="9938b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9938b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9938b-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9938b-129">-Description</span></span>
<span data-ttu-id="9938b-130">A kapcsolat leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9938b-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="9938b-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9938b-131">-Name</span></span>
<span data-ttu-id="9938b-132">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9938b-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="9938b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9938b-133">-ResourceGroupName</span></span>
<span data-ttu-id="9938b-134">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag létrehoz egy kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="9938b-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="9938b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9938b-135">CommonParameters</span></span>
<span data-ttu-id="9938b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9938b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9938b-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9938b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9938b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9938b-138">INPUTS</span></span>

### <span data-ttu-id="9938b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9938b-139">System.String</span></span>

### <span data-ttu-id="9938b-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9938b-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9938b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9938b-141">OUTPUTS</span></span>

### <span data-ttu-id="9938b-142">Microsoft. Azure. Command. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9938b-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9938b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9938b-143">NOTES</span></span>

## <span data-ttu-id="9938b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9938b-144">RELATED LINKS</span></span>

[<span data-ttu-id="9938b-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9938b-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="9938b-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9938b-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


