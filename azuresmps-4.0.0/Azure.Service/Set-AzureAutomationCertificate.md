---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016428"
---
# <span data-ttu-id="d36bd-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d36bd-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="d36bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d36bd-102">SYNOPSIS</span></span>

<span data-ttu-id="d36bd-103">Az automatizálási tanúsítványok konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="d36bd-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="d36bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d36bd-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d36bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d36bd-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d36bd-106">A **set-AzureAutomationCertificate** parancsmag módosítja a tanúsítványok konfigurációját a Microsoft Azure automatizálási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="d36bd-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d36bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d36bd-107">EXAMPLES</span></span>

### <span data-ttu-id="d36bd-108">Példa 1: tanúsítvány frissítése</span><span class="sxs-lookup"><span data-stu-id="d36bd-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="d36bd-109">Ezekkel a parancsokkal frissíthető egy MyCertificate nevű meglévő tanúsítvány az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d36bd-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="d36bd-110">Az első parancs létrehozza a tanúsítványt frissítő második parancsban használt tanúsítványfájl jelszavát.</span><span class="sxs-lookup"><span data-stu-id="d36bd-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="d36bd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d36bd-111">PARAMETERS</span></span>

### <span data-ttu-id="d36bd-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d36bd-112">-AutomationAccountName</span></span>
<span data-ttu-id="d36bd-113">A tanúsítványt használó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36bd-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="d36bd-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d36bd-114">-Description</span></span>
<span data-ttu-id="d36bd-115">A tanúsítvány leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36bd-115">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36bd-116">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="d36bd-116">-Exportable</span></span>
<span data-ttu-id="d36bd-117">Jelzi, hogy a tanúsítvány exportálható.</span><span class="sxs-lookup"><span data-stu-id="d36bd-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36bd-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d36bd-118">-Name</span></span>
<span data-ttu-id="d36bd-119">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36bd-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="d36bd-120">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="d36bd-120">-Password</span></span>
<span data-ttu-id="d36bd-121">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36bd-121">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36bd-122">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d36bd-122">-Path</span></span>
<span data-ttu-id="d36bd-123">A feltölteni kívánt parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36bd-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="d36bd-124">A fájl. cer vagy. pfx formátumú lehet.</span><span class="sxs-lookup"><span data-stu-id="d36bd-124">The file can be .cer or .pfx.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36bd-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d36bd-125">-Profile</span></span>
<span data-ttu-id="d36bd-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d36bd-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d36bd-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d36bd-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d36bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36bd-128">CommonParameters</span></span>
<span data-ttu-id="d36bd-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d36bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36bd-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36bd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36bd-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d36bd-131">INPUTS</span></span>

## <span data-ttu-id="d36bd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d36bd-132">OUTPUTS</span></span>

### <span data-ttu-id="d36bd-133">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="d36bd-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d36bd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d36bd-134">NOTES</span></span>

## <span data-ttu-id="d36bd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d36bd-135">RELATED LINKS</span></span>

[<span data-ttu-id="d36bd-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d36bd-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="d36bd-137">Új – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d36bd-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="d36bd-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d36bd-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


