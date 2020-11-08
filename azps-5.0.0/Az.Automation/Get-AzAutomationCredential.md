---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186136"
---
# <span data-ttu-id="6730d-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6730d-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="6730d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6730d-102">SYNOPSIS</span></span>
<span data-ttu-id="6730d-103">Automatizálási hitelesítő adatok jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="6730d-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="6730d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6730d-104">SYNTAX</span></span>

### <span data-ttu-id="6730d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6730d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6730d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6730d-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6730d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6730d-107">DESCRIPTION</span></span>
<span data-ttu-id="6730d-108">A **Get-AzAutomationCredential** parancsmag egy vagy több Azure Automation hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="6730d-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="6730d-109">Alapértelmezés szerint minden hitelesítő adatot visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6730d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="6730d-110">Adja meg a hitelesítő adatokhoz tartozó hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="6730d-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="6730d-111">Biztonsági okokból ez a parancsmag nem adja meg a hitelesítő adatok jelszavát.</span><span class="sxs-lookup"><span data-stu-id="6730d-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="6730d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6730d-112">EXAMPLES</span></span>

### <span data-ttu-id="6730d-113">Példa 1: a hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="6730d-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6730d-114">Ez a parancs a Contoso17 nevű automatizálási fiók összes hitelesítő adatainak metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="6730d-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6730d-115">2. példa: hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="6730d-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="6730d-116">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoCredential nevű hitelesítő adatainak metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6730d-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6730d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6730d-117">PARAMETERS</span></span>

### <span data-ttu-id="6730d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6730d-118">-AutomationAccountName</span></span>
<span data-ttu-id="6730d-119">Annak az automatizálási fióknak a neve, amelyhez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="6730d-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6730d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6730d-120">-DefaultProfile</span></span>
<span data-ttu-id="6730d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6730d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6730d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6730d-122">-Name</span></span>
<span data-ttu-id="6730d-123">A lekérdezni kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6730d-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6730d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6730d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6730d-125">Azt az erőforráscsoportot adja meg, amelyhez ez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="6730d-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6730d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6730d-126">CommonParameters</span></span>
<span data-ttu-id="6730d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6730d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6730d-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6730d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6730d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6730d-129">INPUTS</span></span>

### <span data-ttu-id="6730d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6730d-130">System.String</span></span>

## <span data-ttu-id="6730d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6730d-131">OUTPUTS</span></span>

### <span data-ttu-id="6730d-132">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6730d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6730d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6730d-133">NOTES</span></span>

## <span data-ttu-id="6730d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6730d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6730d-135">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6730d-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="6730d-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6730d-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="6730d-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6730d-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)

