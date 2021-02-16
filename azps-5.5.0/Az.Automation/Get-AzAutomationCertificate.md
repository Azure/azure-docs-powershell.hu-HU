---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168459"
---
# <span data-ttu-id="2e21e-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e21e-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="2e21e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e21e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e21e-103">Automatizálási tanúsítványokat kap.</span><span class="sxs-lookup"><span data-stu-id="2e21e-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="2e21e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e21e-104">SYNTAX</span></span>

### <span data-ttu-id="2e21e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e21e-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e21e-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="2e21e-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e21e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e21e-107">DESCRIPTION</span></span>
<span data-ttu-id="2e21e-108">A **Get-AzAutomationCertificate** parancsmag egy vagy több Azure Automation-tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="2e21e-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="2e21e-109">Alapértelmezés szerint ez a parancsmag az összes tanúsítványt megkapja.</span><span class="sxs-lookup"><span data-stu-id="2e21e-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="2e21e-110">Adja meg egy tanúsítvány nevét, ha egy adott tanúsítványt be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="2e21e-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="2e21e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e21e-111">EXAMPLES</span></span>

### <span data-ttu-id="2e21e-112">1. példa: Az összes tanúsítvány lekérte</span><span class="sxs-lookup"><span data-stu-id="2e21e-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="2e21e-113">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="2e21e-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2e21e-114">2. példa: Tanúsítvány lekérve</span><span class="sxs-lookup"><span data-stu-id="2e21e-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="2e21e-115">Ez a parancs a ContosoCertificate nevű tanúsítvány metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="2e21e-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="2e21e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e21e-116">PARAMETERS</span></span>

### <span data-ttu-id="2e21e-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e21e-117">-AutomationAccountName</span></span>
<span data-ttu-id="2e21e-118">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja tanúsítványt olvassa be.</span><span class="sxs-lookup"><span data-stu-id="2e21e-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="2e21e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e21e-119">-DefaultProfile</span></span>
<span data-ttu-id="2e21e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e21e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e21e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2e21e-121">-Name</span></span>
<span data-ttu-id="2e21e-122">A visszakeresni szükséges tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e21e-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e21e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e21e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e21e-124">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="2e21e-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="2e21e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e21e-125">CommonParameters</span></span>
<span data-ttu-id="2e21e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e21e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e21e-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e21e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e21e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e21e-128">INPUTS</span></span>

### <span data-ttu-id="2e21e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2e21e-129">System.String</span></span>

## <span data-ttu-id="2e21e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e21e-130">OUTPUTS</span></span>

### <span data-ttu-id="2e21e-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="2e21e-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="2e21e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e21e-132">NOTES</span></span>

## <span data-ttu-id="2e21e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e21e-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e21e-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e21e-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="2e21e-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e21e-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="2e21e-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2e21e-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


