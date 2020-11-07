---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 956569d407918d0891af6aa1d6f8f09eb61b9a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679987"
---
# <span data-ttu-id="6beca-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6beca-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="6beca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6beca-102">SYNOPSIS</span></span>
<span data-ttu-id="6beca-103">Automatizálási tanúsítványokat kap.</span><span class="sxs-lookup"><span data-stu-id="6beca-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6beca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6beca-104">SYNTAX</span></span>

### <span data-ttu-id="6beca-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6beca-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6beca-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="6beca-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6beca-107">DESCRIPTION</span></span>
<span data-ttu-id="6beca-108">A **Get-AzureRmAutomationCertificate** parancsmag egy vagy több Azure automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="6beca-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="6beca-109">Alapértelmezés szerint ez a parancsmag minden tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="6beca-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="6beca-110">Adja meg a tanúsítvány nevét egy adott tanúsítvány beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="6beca-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="6beca-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6beca-111">EXAMPLES</span></span>

### <span data-ttu-id="6beca-112">Példa 1: az összes tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="6beca-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6beca-113">Ez a parancs a Contoso17 nevű automatizálási fiók összes tanúsítványához metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="6beca-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6beca-114">2. példa: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="6beca-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="6beca-115">Ez a parancs a ContosoCertificate nevű tanúsítvány metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6beca-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="6beca-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6beca-116">PARAMETERS</span></span>

### <span data-ttu-id="6beca-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6beca-117">-AutomationAccountName</span></span>
<span data-ttu-id="6beca-118">Annak az automatizálási fióknak a neve, amelyhez a parancsmag Kinyeri a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="6beca-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="6beca-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6beca-119">-Name</span></span>
<span data-ttu-id="6beca-120">A beolvasandó tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6beca-120">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="6beca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beca-121">-ResourceGroupName</span></span>
<span data-ttu-id="6beca-122">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="6beca-122">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="6beca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beca-123">-DefaultProfile</span></span>
<span data-ttu-id="6beca-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6beca-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6beca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beca-125">CommonParameters</span></span>
<span data-ttu-id="6beca-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6beca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beca-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6beca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beca-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6beca-128">INPUTS</span></span>

## <span data-ttu-id="6beca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6beca-129">OUTPUTS</span></span>

### <span data-ttu-id="6beca-130">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="6beca-130">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="6beca-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6beca-131">NOTES</span></span>

## <span data-ttu-id="6beca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6beca-132">RELATED LINKS</span></span>

[<span data-ttu-id="6beca-133">Új – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6beca-133">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6beca-134">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6beca-134">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6beca-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6beca-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


