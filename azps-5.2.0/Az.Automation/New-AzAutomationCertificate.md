---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373573"
---
# <span data-ttu-id="c3fb6-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fb6-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="c3fb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb6-103">Automatizálási tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="c3fb6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3fb6-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3fb6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="c3fb6-106">A **New-AzAutomationCertificate** parancsmag létrehoz egy tanúsítványt az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="c3fb6-107">Adja meg a feltölthet tanúsítványfájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="c3fb6-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3fb6-108">EXAMPLES</span></span>

### <span data-ttu-id="c3fb6-109">1. példa: Új tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="c3fb6-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c3fb6-110">Az első parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c3fb6-111">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="c3fb6-112">A második parancs létrehoz egy ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="c3fb6-113">A parancs a $Password.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="c3fb6-114">A parancs megadja a fiók nevét és a feltöltött fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="c3fb6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3fb6-115">PARAMETERS</span></span>

### <span data-ttu-id="c3fb6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3fb6-116">-AutomationAccountName</span></span>
<span data-ttu-id="c3fb6-117">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="c3fb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fb6-118">-DefaultProfile</span></span>
<span data-ttu-id="c3fb6-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c3fb6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3fb6-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c3fb6-120">-Description</span></span>
<span data-ttu-id="c3fb6-121">Megadja a tanúsítvány leírását.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="c3fb6-122">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="c3fb6-122">-Exportable</span></span>
<span data-ttu-id="c3fb6-123">Azt adja meg, hogy exportálható-e a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="c3fb6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fb6-124">-Name</span></span>
<span data-ttu-id="c3fb6-125">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="c3fb6-126">-Password</span><span class="sxs-lookup"><span data-stu-id="c3fb6-126">-Password</span></span>
<span data-ttu-id="c3fb6-127">Megadja a tanúsítványfájl jelszavát.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="c3fb6-128">-Path</span><span class="sxs-lookup"><span data-stu-id="c3fb6-128">-Path</span></span>
<span data-ttu-id="c3fb6-129">A parancsmag által feltöltött parancsfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="c3fb6-130">A fájl lehet .cer vagy .pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="c3fb6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fb6-131">-ResourceGroupName</span></span>
<span data-ttu-id="c3fb6-132">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a parancsmag tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="c3fb6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb6-133">CommonParameters</span></span>
<span data-ttu-id="c3fb6-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fb6-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fb6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3fb6-136">INPUTS</span></span>

### <span data-ttu-id="c3fb6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c3fb6-137">System.String</span></span>

### <span data-ttu-id="c3fb6-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c3fb6-138">System.Security.SecureString</span></span>

### <span data-ttu-id="c3fb6-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3fb6-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3fb6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fb6-140">OUTPUTS</span></span>

### <span data-ttu-id="c3fb6-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="c3fb6-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="c3fb6-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3fb6-142">NOTES</span></span>

<span data-ttu-id="c3fb6-143">Ezt a parancsot olyan számítógépen kell futtatni, amely rendszergazdája, valamint emelt szintű PowerShell-munkamenetben; A tanúsítvány feltöltése előtt ez a parancsmag a helyi X.509 tárolót használja a thumbprint és a kulcs beolvasására, és ha a parancsmag egy emelt szintű PowerShell-munkameneten kívül fut, "Access denied" (Hozzáférés megtagadva) hibaüzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="c3fb6-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="c3fb6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3fb6-144">RELATED LINKS</span></span>

[<span data-ttu-id="c3fb6-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fb6-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="c3fb6-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fb6-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="c3fb6-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fb6-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


