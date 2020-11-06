---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 549bc5bb67eab5287bf463f7e816cc0ff597cf52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494186"
---
# <span data-ttu-id="3347d-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3347d-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="3347d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3347d-102">SYNOPSIS</span></span>
<span data-ttu-id="3347d-103">Az automatizálási tanúsítványok konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="3347d-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3347d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3347d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3347d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3347d-105">DESCRIPTION</span></span>
<span data-ttu-id="3347d-106">A **set-AzureRmAutomationCertificate** parancsmag a tanúsítványok konfigurációját az Azure automatizálásban módosítja.</span><span class="sxs-lookup"><span data-stu-id="3347d-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="3347d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3347d-107">EXAMPLES</span></span>

### <span data-ttu-id="3347d-108">Példa 1: tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="3347d-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3347d-109">Az első parancs az egyszerű szöveges jelszót biztonságos karakterláncként konvertálja az ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3347d-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3347d-110">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3347d-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3347d-111">A második parancs módosította a ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3347d-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="3347d-112">A parancs a $Passwordban tárolt jelszót használja.</span><span class="sxs-lookup"><span data-stu-id="3347d-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="3347d-113">A parancs a fiók nevét és a feltöltött fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347d-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="3347d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3347d-114">PARAMETERS</span></span>

### <span data-ttu-id="3347d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3347d-115">-AutomationAccountName</span></span>
<span data-ttu-id="3347d-116">Annak az automatizálási fióknak a neve, amelyhez a parancsmag módosította a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3347d-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="3347d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3347d-117">-DefaultProfile</span></span>
<span data-ttu-id="3347d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3347d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3347d-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3347d-119">-Description</span></span>
<span data-ttu-id="3347d-120">A parancsmag által módosított tanúsítvány leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347d-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3347d-121">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="3347d-121">-Exportable</span></span>
<span data-ttu-id="3347d-122">Meghatározza, hogy a tanúsítvány exportálható-e.</span><span class="sxs-lookup"><span data-stu-id="3347d-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3347d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3347d-123">-Name</span></span>
<span data-ttu-id="3347d-124">Annak a tanúsítványnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3347d-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3347d-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3347d-125">-Password</span></span>
<span data-ttu-id="3347d-126">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347d-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3347d-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3347d-127">-Path</span></span>
<span data-ttu-id="3347d-128">A feltölteni kívánt parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347d-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="3347d-129">A fájl lehet. cer vagy. pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="3347d-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="3347d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3347d-130">-ResourceGroupName</span></span>
<span data-ttu-id="3347d-131">Annak az erőforráscsoport a neve, amelyhez a parancsmag módosította a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3347d-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="3347d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3347d-132">CommonParameters</span></span>
<span data-ttu-id="3347d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3347d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3347d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3347d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3347d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3347d-135">INPUTS</span></span>

### <span data-ttu-id="3347d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3347d-136">System.String</span></span>

### <span data-ttu-id="3347d-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3347d-137">System.Security.SecureString</span></span>

### <span data-ttu-id="3347d-138">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3347d-138">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3347d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3347d-139">OUTPUTS</span></span>

### <span data-ttu-id="3347d-140">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3347d-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3347d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3347d-141">NOTES</span></span>

## <span data-ttu-id="3347d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3347d-142">RELATED LINKS</span></span>

[<span data-ttu-id="3347d-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3347d-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3347d-144">Új – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3347d-144">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3347d-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3347d-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


