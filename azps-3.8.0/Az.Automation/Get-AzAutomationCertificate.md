---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012722"
---
# <span data-ttu-id="aaedb-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="aaedb-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="aaedb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aaedb-102">SYNOPSIS</span></span>
<span data-ttu-id="aaedb-103">Automatizálási tanúsítványokat kap.</span><span class="sxs-lookup"><span data-stu-id="aaedb-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="aaedb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aaedb-104">SYNTAX</span></span>

### <span data-ttu-id="aaedb-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aaedb-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaedb-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="aaedb-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaedb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aaedb-107">DESCRIPTION</span></span>
<span data-ttu-id="aaedb-108">A **Get-AzAutomationCertificate** parancsmag egy vagy több Azure automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="aaedb-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="aaedb-109">Alapértelmezés szerint ez a parancsmag minden tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="aaedb-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="aaedb-110">Adja meg a tanúsítvány nevét egy adott tanúsítvány beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="aaedb-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="aaedb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="aaedb-111">EXAMPLES</span></span>

### <span data-ttu-id="aaedb-112">Példa 1: az összes tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="aaedb-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="aaedb-113">Ez a parancs a Contoso17 nevű automatizálási fiók összes tanúsítványához metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="aaedb-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="aaedb-114">2. példa: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="aaedb-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="aaedb-115">Ez a parancs a ContosoCertificate nevű tanúsítvány metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aaedb-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="aaedb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aaedb-116">PARAMETERS</span></span>

### <span data-ttu-id="aaedb-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aaedb-117">-AutomationAccountName</span></span>
<span data-ttu-id="aaedb-118">Annak az automatizálási fióknak a neve, amelyhez a parancsmag Kinyeri a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="aaedb-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="aaedb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaedb-119">-DefaultProfile</span></span>
<span data-ttu-id="aaedb-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aaedb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaedb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aaedb-121">-Name</span></span>
<span data-ttu-id="aaedb-122">A beolvasandó tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aaedb-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="aaedb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaedb-123">-ResourceGroupName</span></span>
<span data-ttu-id="aaedb-124">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="aaedb-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="aaedb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaedb-125">CommonParameters</span></span>
<span data-ttu-id="aaedb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aaedb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaedb-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaedb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaedb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaedb-128">INPUTS</span></span>

### <span data-ttu-id="aaedb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aaedb-129">System.String</span></span>

## <span data-ttu-id="aaedb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaedb-130">OUTPUTS</span></span>

### <span data-ttu-id="aaedb-131">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="aaedb-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="aaedb-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aaedb-132">NOTES</span></span>

## <span data-ttu-id="aaedb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaedb-133">RELATED LINKS</span></span>

[<span data-ttu-id="aaedb-134">Új – AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="aaedb-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="aaedb-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="aaedb-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="aaedb-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="aaedb-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


