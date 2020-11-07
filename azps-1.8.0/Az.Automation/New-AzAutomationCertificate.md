---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 1c3c3cb4fecfde01926e21a75470fc945f8c86c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671570"
---
# <span data-ttu-id="0abfc-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abfc-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="0abfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0abfc-102">SYNOPSIS</span></span>
<span data-ttu-id="0abfc-103">Automatizálási tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0abfc-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="0abfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0abfc-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0abfc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0abfc-105">DESCRIPTION</span></span>
<span data-ttu-id="0abfc-106">A **New-AzAutomationCertificate** parancsmag létrehoz egy tanúsítványt az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="0abfc-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="0abfc-107">A feltölteni kívánt tanúsítványfájl elérési útjának megadása</span><span class="sxs-lookup"><span data-stu-id="0abfc-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="0abfc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0abfc-108">EXAMPLES</span></span>

### <span data-ttu-id="0abfc-109">Példa 1: új tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="0abfc-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0abfc-110">Az első parancs az egyszerű szöveges jelszót biztonságos karakterláncként konvertálja az ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0abfc-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0abfc-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0abfc-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="0abfc-112">A második parancs létrehoz egy ContosoCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="0abfc-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="0abfc-113">A parancs a $Passwordban tárolt jelszót használja.</span><span class="sxs-lookup"><span data-stu-id="0abfc-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="0abfc-114">A parancs a fiók nevét és a feltöltött fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="0abfc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0abfc-115">PARAMETERS</span></span>

### <span data-ttu-id="0abfc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0abfc-116">-AutomationAccountName</span></span>
<span data-ttu-id="0abfc-117">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a tanúsítványt tárolja.</span><span class="sxs-lookup"><span data-stu-id="0abfc-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="0abfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abfc-118">-DefaultProfile</span></span>
<span data-ttu-id="0abfc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0abfc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0abfc-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0abfc-120">-Description</span></span>
<span data-ttu-id="0abfc-121">A tanúsítvány leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="0abfc-122">-Exportálható</span><span class="sxs-lookup"><span data-stu-id="0abfc-122">-Exportable</span></span>
<span data-ttu-id="0abfc-123">Meghatározza, hogy a tanúsítvány exportálható-e.</span><span class="sxs-lookup"><span data-stu-id="0abfc-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="0abfc-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0abfc-124">-Name</span></span>
<span data-ttu-id="0abfc-125">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="0abfc-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="0abfc-126">-Password</span></span>
<span data-ttu-id="0abfc-127">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="0abfc-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0abfc-128">-Path</span></span>
<span data-ttu-id="0abfc-129">A parancsmag által feltöltött parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="0abfc-130">A fájl lehet. cer vagy. pfx fájl.</span><span class="sxs-lookup"><span data-stu-id="0abfc-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="0abfc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abfc-131">-ResourceGroupName</span></span>
<span data-ttu-id="0abfc-132">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="0abfc-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="0abfc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abfc-133">CommonParameters</span></span>
<span data-ttu-id="0abfc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0abfc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abfc-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0abfc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abfc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0abfc-136">INPUTS</span></span>

### <span data-ttu-id="0abfc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0abfc-137">System.String</span></span>

### <span data-ttu-id="0abfc-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0abfc-138">System.Security.SecureString</span></span>

### <span data-ttu-id="0abfc-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0abfc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0abfc-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0abfc-140">OUTPUTS</span></span>

### <span data-ttu-id="0abfc-141">Microsoft. Azure. Command. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0abfc-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0abfc-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0abfc-142">NOTES</span></span>

<span data-ttu-id="0abfc-143">Ezt a parancsot egy olyan gépen kell futtatni, amelyen Ön a rendszergazda, valamint egy magasabb PowerShell-munkamenetben. a tanúsítvány feltöltése előtt ez a parancsmag a helyi X. 509 tárolót használja az ujjlenyomat és a kulcs beolvasásához, illetve ha ez a parancsmag egy magasabb PowerShell-munkameneten kívül fut, a "hozzáférés megtagadva" hibaüzenet jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0abfc-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="0abfc-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0abfc-144">RELATED LINKS</span></span>

[<span data-ttu-id="0abfc-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abfc-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="0abfc-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abfc-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="0abfc-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abfc-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


