---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010902"
---
# <span data-ttu-id="b5a47-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b5a47-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="b5a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a47-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a47-103">Automatizálási tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5a47-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="b5a47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5a47-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a47-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5a47-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a47-106">A **New-AzAutomationCertificate** parancsmag létrehoz egy tanúsítványt az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="b5a47-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="b5a47-107">Adja meg a feltölthet tanúsítványfájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="b5a47-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="b5a47-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5a47-108">EXAMPLES</span></span>

### <span data-ttu-id="b5a47-109">1. példa: Új tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5a47-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b5a47-110">Az első parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b5a47-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="b5a47-111">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a47-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="b5a47-112">A második parancs létrehoz egy ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b5a47-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="b5a47-113">A parancs a $Password.</span><span class="sxs-lookup"><span data-stu-id="b5a47-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="b5a47-114">A parancs megadja a fiók nevét és a feltöltött fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="b5a47-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="b5a47-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5a47-115">PARAMETERS</span></span>

### <span data-ttu-id="b5a47-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5a47-116">-AutomationAccountName</span></span>
<span data-ttu-id="b5a47-117">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b5a47-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="b5a47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a47-118">-DefaultProfile</span></span>
<span data-ttu-id="b5a47-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5a47-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5a47-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b5a47-120">-Description</span></span>
<span data-ttu-id="b5a47-121">Megadja a tanúsítvány leírását.</span><span class="sxs-lookup"><span data-stu-id="b5a47-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="b5a47-122">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="b5a47-122">-Exportable</span></span>
<span data-ttu-id="b5a47-123">Azt adja meg, hogy exportálható-e a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="b5a47-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a47-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b5a47-124">-Name</span></span>
<span data-ttu-id="b5a47-125">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a47-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="b5a47-126">-Password</span><span class="sxs-lookup"><span data-stu-id="b5a47-126">-Password</span></span>
<span data-ttu-id="b5a47-127">Megadja a tanúsítványfájl jelszavát.</span><span class="sxs-lookup"><span data-stu-id="b5a47-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="b5a47-128">-Path</span><span class="sxs-lookup"><span data-stu-id="b5a47-128">-Path</span></span>
<span data-ttu-id="b5a47-129">A parancsmag által feltöltött parancsfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a47-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="b5a47-130">A fájl lehet .cer vagy .pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="b5a47-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="b5a47-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a47-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5a47-132">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5a47-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="b5a47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a47-133">CommonParameters</span></span>
<span data-ttu-id="b5a47-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a47-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a47-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a47-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5a47-136">INPUTS</span></span>

### <span data-ttu-id="b5a47-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a47-137">System.String</span></span>

### <span data-ttu-id="b5a47-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b5a47-138">System.Security.SecureString</span></span>

### <span data-ttu-id="b5a47-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b5a47-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b5a47-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a47-140">OUTPUTS</span></span>

### <span data-ttu-id="b5a47-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="b5a47-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="b5a47-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5a47-142">NOTES</span></span>

<span data-ttu-id="b5a47-143">Ezt a parancsot olyan számítógépen kell futtatni, amely rendszergazdája, valamint emelt szintű PowerShell-munkamenetben; A tanúsítvány feltöltése előtt ez a parancsmag a helyi X.509 tárolót használja a thumbprint és a kulcs beolvasására, és ha a parancsmag egy emelt szintű PowerShell-munkameneten kívül fut, "Access denied" (Hozzáférés megtagadva) hibaüzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="b5a47-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="b5a47-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5a47-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5a47-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b5a47-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="b5a47-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b5a47-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="b5a47-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b5a47-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


