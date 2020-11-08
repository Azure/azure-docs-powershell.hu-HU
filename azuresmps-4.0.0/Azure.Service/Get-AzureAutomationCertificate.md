---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015663"
---
# <span data-ttu-id="cbaf7-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cbaf7-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="cbaf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbaf7-102">SYNOPSIS</span></span>

<span data-ttu-id="cbaf7-103">Azure automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="cbaf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbaf7-104">SYNTAX</span></span>

### <span data-ttu-id="cbaf7-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbaf7-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cbaf7-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="cbaf7-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbaf7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbaf7-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cbaf7-108">A **Get-AzureAutomationCertificate** parancsmag egy vagy több Microsoft Azure automatizálási tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="cbaf7-109">Alapértelmezés szerint minden tanúsítvány visszaadva van.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="cbaf7-110">Egy adott tanúsítvány beszerzéséhez adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="cbaf7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cbaf7-111">EXAMPLES</span></span>

### <span data-ttu-id="cbaf7-112">Példa 1: az összes tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="cbaf7-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cbaf7-113">Ez a parancs a Contoso17 nevű Azure Automation fiók minden tanúsítványát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="cbaf7-114">2. példa: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="cbaf7-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="cbaf7-115">Ez a parancs a MyUserCertificate nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="cbaf7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbaf7-116">PARAMETERS</span></span>

### <span data-ttu-id="cbaf7-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cbaf7-117">-AutomationAccountName</span></span>
<span data-ttu-id="cbaf7-118">A tanúsítványt használó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-118">Specifies the name of the automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbaf7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbaf7-119">-Name</span></span>
<span data-ttu-id="cbaf7-120">A beolvasandó tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbaf7-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="cbaf7-121">-Profile</span></span>
<span data-ttu-id="cbaf7-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbaf7-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cbaf7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbaf7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbaf7-124">CommonParameters</span></span>
<span data-ttu-id="cbaf7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbaf7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbaf7-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbaf7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbaf7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbaf7-127">INPUTS</span></span>

## <span data-ttu-id="cbaf7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbaf7-128">OUTPUTS</span></span>

### <span data-ttu-id="cbaf7-129">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="cbaf7-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="cbaf7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbaf7-130">NOTES</span></span>

## <span data-ttu-id="cbaf7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbaf7-131">RELATED LINKS</span></span>

[<span data-ttu-id="cbaf7-132">Új – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cbaf7-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="cbaf7-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cbaf7-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="cbaf7-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cbaf7-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


