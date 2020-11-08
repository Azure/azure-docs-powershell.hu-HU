---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016222"
---
# <span data-ttu-id="ffb87-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb87-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ffb87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffb87-102">SYNOPSIS</span></span>

<span data-ttu-id="ffb87-103">Azure automatizálási tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ffb87-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="ffb87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffb87-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ffb87-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffb87-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ffb87-106">A **New-AzureAutomationCertificate** parancsmag létrehoz egy tanúsítványt a Microsoft Azure automatizálási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="ffb87-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="ffb87-107">Megadja a feltölteni kívánt tanúsítványfájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="ffb87-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="ffb87-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ffb87-108">EXAMPLES</span></span>

### <span data-ttu-id="ffb87-109">Példa 1: tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="ffb87-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="ffb87-110">Ezek a parancsok az Azure Automation MyCertificate nevű tanúsítványát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ffb87-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="ffb87-111">Az első parancs létrehozza a tanúsítványt létrehozó második parancsban használt tanúsítványfájl jelszavát.</span><span class="sxs-lookup"><span data-stu-id="ffb87-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="ffb87-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffb87-112">PARAMETERS</span></span>

### <span data-ttu-id="ffb87-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ffb87-113">-AutomationAccountName</span></span>
<span data-ttu-id="ffb87-114">Itt adhatja meg annak az automatizálási fióknak a nevét, amelyet a rendszer tárol a tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="ffb87-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="ffb87-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ffb87-115">-Description</span></span>
<span data-ttu-id="ffb87-116">A tanúsítvány leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffb87-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="ffb87-117">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="ffb87-117">-Exportable</span></span>
<span data-ttu-id="ffb87-118">Jelzi, hogy a tanúsítvány exportálható.</span><span class="sxs-lookup"><span data-stu-id="ffb87-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb87-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffb87-119">-Name</span></span>
<span data-ttu-id="ffb87-120">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffb87-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="ffb87-121">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="ffb87-121">-Password</span></span>
<span data-ttu-id="ffb87-122">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffb87-122">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="ffb87-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ffb87-123">-Path</span></span>
<span data-ttu-id="ffb87-124">A feltölteni kívánt parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffb87-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="ffb87-125">A fájl. cer vagy. pfx formátumú lehet.</span><span class="sxs-lookup"><span data-stu-id="ffb87-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="ffb87-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="ffb87-126">-Profile</span></span>
<span data-ttu-id="ffb87-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ffb87-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffb87-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ffb87-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffb87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb87-129">CommonParameters</span></span>
<span data-ttu-id="ffb87-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffb87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb87-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb87-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb87-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffb87-132">INPUTS</span></span>

## <span data-ttu-id="ffb87-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffb87-133">OUTPUTS</span></span>

### <span data-ttu-id="ffb87-134">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ffb87-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ffb87-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffb87-135">NOTES</span></span>

## <span data-ttu-id="ffb87-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffb87-136">RELATED LINKS</span></span>

[<span data-ttu-id="ffb87-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb87-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="ffb87-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb87-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="ffb87-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb87-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


