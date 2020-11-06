---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492400"
---
# <span data-ttu-id="a4926-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4926-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="a4926-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4926-102">SYNOPSIS</span></span>
<span data-ttu-id="a4926-103">Automatizálási tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4926-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4926-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4926-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4926-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4926-105">DESCRIPTION</span></span>
<span data-ttu-id="a4926-106">A **New-AzureRmAutomationCertificate** parancsmag létrehoz egy tanúsítványt az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a4926-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="a4926-107">A feltölteni kívánt tanúsítványfájl elérési útjának megadása</span><span class="sxs-lookup"><span data-stu-id="a4926-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="a4926-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a4926-108">EXAMPLES</span></span>

### <span data-ttu-id="a4926-109">Példa 1: új tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="a4926-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4926-110">Az első parancs az egyszerű szöveges jelszót biztonságos karakterláncként konvertálja az ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a4926-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a4926-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4926-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="a4926-112">A második parancs létrehoz egy ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a4926-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="a4926-113">A parancs a $Passwordban tárolt jelszót használja.</span><span class="sxs-lookup"><span data-stu-id="a4926-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="a4926-114">A parancs a fiók nevét és a feltöltött fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4926-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="a4926-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4926-115">PARAMETERS</span></span>

### <span data-ttu-id="a4926-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4926-116">-AutomationAccountName</span></span>
<span data-ttu-id="a4926-117">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a tanúsítványt tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4926-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4926-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4926-118">-DefaultProfile</span></span>
<span data-ttu-id="a4926-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a4926-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4926-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a4926-120">-Description</span></span>
<span data-ttu-id="a4926-121">A tanúsítvány leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4926-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="a4926-122">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="a4926-122">-Exportable</span></span>
<span data-ttu-id="a4926-123">Meghatározza, hogy a tanúsítvány exportálható-e.</span><span class="sxs-lookup"><span data-stu-id="a4926-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="a4926-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4926-124">-Name</span></span>
<span data-ttu-id="a4926-125">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4926-125">Specifies the name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4926-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="a4926-126">-Password</span></span>
<span data-ttu-id="a4926-127">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4926-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="a4926-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a4926-128">-Path</span></span>
<span data-ttu-id="a4926-129">A parancsmag által feltöltött parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4926-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="a4926-130">A fájl lehet. cer vagy. pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="a4926-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4926-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4926-131">-ResourceGroupName</span></span>
<span data-ttu-id="a4926-132">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a4926-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4926-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4926-133">CommonParameters</span></span>
<span data-ttu-id="a4926-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4926-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4926-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4926-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4926-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4926-136">INPUTS</span></span>

### <span data-ttu-id="a4926-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4926-137">None</span></span>
<span data-ttu-id="a4926-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a4926-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4926-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4926-139">OUTPUTS</span></span>

### <span data-ttu-id="a4926-140">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="a4926-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a4926-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4926-141">NOTES</span></span>

## <span data-ttu-id="a4926-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4926-142">RELATED LINKS</span></span>

[<span data-ttu-id="a4926-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4926-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="a4926-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4926-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="a4926-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4926-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


