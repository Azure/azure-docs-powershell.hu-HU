---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373139"
---
# <span data-ttu-id="35c4c-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="35c4c-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="35c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="35c4c-103">Módosítja egy automatizálási tanúsítvány konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="35c4c-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="35c4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35c4c-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c4c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="35c4c-106">A **Set-AzAutomationCertificate** parancsmag módosítja egy tanúsítvány konfigurációját az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="35c4c-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="35c4c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="35c4c-108">1. példa: Tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="35c4c-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="35c4c-109">Az első parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="35c4c-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="35c4c-110">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="35c4c-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="35c4c-111">A második parancs módosítja a ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="35c4c-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="35c4c-112">A parancs a $Password.</span><span class="sxs-lookup"><span data-stu-id="35c4c-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="35c4c-113">A parancs megadja a fiók nevét és a feltöltött fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="35c4c-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="35c4c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35c4c-114">PARAMETERS</span></span>

### <span data-ttu-id="35c4c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35c4c-115">-AutomationAccountName</span></span>
<span data-ttu-id="35c4c-116">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja módosítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="35c4c-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="35c4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c4c-117">-DefaultProfile</span></span>
<span data-ttu-id="35c4c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35c4c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35c4c-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="35c4c-119">-Description</span></span>
<span data-ttu-id="35c4c-120">Megadja annak a tanúsítványnak a leírását, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="35c4c-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35c4c-121">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="35c4c-121">-Exportable</span></span>
<span data-ttu-id="35c4c-122">Azt adja meg, hogy exportálható-e a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="35c4c-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="35c4c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35c4c-123">-Name</span></span>
<span data-ttu-id="35c4c-124">A parancsmag által módosított tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="35c4c-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35c4c-125">-Password</span><span class="sxs-lookup"><span data-stu-id="35c4c-125">-Password</span></span>
<span data-ttu-id="35c4c-126">Megadja a tanúsítványfájl jelszavát.</span><span class="sxs-lookup"><span data-stu-id="35c4c-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="35c4c-127">-Path</span><span class="sxs-lookup"><span data-stu-id="35c4c-127">-Path</span></span>
<span data-ttu-id="35c4c-128">A feltöltni kívánt parancsfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c4c-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="35c4c-129">A fájl lehet .cer vagy .pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="35c4c-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="35c4c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c4c-130">-ResourceGroupName</span></span>
<span data-ttu-id="35c4c-131">Annak az erőforráscsoportnak a neve, amelynek a parancsmagja módosítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="35c4c-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="35c4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c4c-132">CommonParameters</span></span>
<span data-ttu-id="35c4c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c4c-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c4c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c4c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35c4c-135">INPUTS</span></span>

### <span data-ttu-id="35c4c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="35c4c-136">System.String</span></span>

### <span data-ttu-id="35c4c-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="35c4c-137">System.Security.SecureString</span></span>

### <span data-ttu-id="35c4c-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35c4c-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="35c4c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35c4c-139">OUTPUTS</span></span>

### <span data-ttu-id="35c4c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="35c4c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="35c4c-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35c4c-141">NOTES</span></span>

## <span data-ttu-id="35c4c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35c4c-142">RELATED LINKS</span></span>

[<span data-ttu-id="35c4c-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="35c4c-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="35c4c-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="35c4c-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="35c4c-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="35c4c-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


