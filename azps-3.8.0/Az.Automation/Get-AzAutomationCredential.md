---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012713"
---
# <span data-ttu-id="8b6a3-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b6a3-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="8b6a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6a3-103">Automatizálási hitelesítő adatok jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="8b6a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b6a3-104">SYNTAX</span></span>

### <span data-ttu-id="8b6a3-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b6a3-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b6a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b6a3-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b6a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="8b6a3-108">A **Get-AzAutomationCredential** parancsmag egy vagy több Azure Automation hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="8b6a3-109">Alapértelmezés szerint minden hitelesítő adatot visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="8b6a3-110">Adja meg a hitelesítő adatokhoz tartozó hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="8b6a3-111">Biztonsági okokból ez a parancsmag nem adja meg a hitelesítő adatok jelszavát.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="8b6a3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8b6a3-112">EXAMPLES</span></span>

### <span data-ttu-id="8b6a3-113">Példa 1: a hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="8b6a3-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8b6a3-114">Ez a parancs a Contoso17 nevű automatizálási fiók összes hitelesítő adatainak metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8b6a3-115">2. példa: hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="8b6a3-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="8b6a3-116">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoCredential nevű hitelesítő adatainak metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8b6a3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b6a3-117">PARAMETERS</span></span>

### <span data-ttu-id="8b6a3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b6a3-118">-AutomationAccountName</span></span>
<span data-ttu-id="8b6a3-119">Annak az automatizálási fióknak a neve, amelyhez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="8b6a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6a3-120">-DefaultProfile</span></span>
<span data-ttu-id="8b6a3-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8b6a3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b6a3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b6a3-122">-Name</span></span>
<span data-ttu-id="8b6a3-123">A lekérdezni kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="8b6a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b6a3-125">Azt az erőforráscsoportot adja meg, amelyhez ez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="8b6a3-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="8b6a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6a3-126">CommonParameters</span></span>
<span data-ttu-id="8b6a3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b6a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6a3-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b6a3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6a3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b6a3-129">INPUTS</span></span>

### <span data-ttu-id="8b6a3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8b6a3-130">System.String</span></span>

## <span data-ttu-id="8b6a3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b6a3-131">OUTPUTS</span></span>

### <span data-ttu-id="8b6a3-132">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="8b6a3-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="8b6a3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b6a3-133">NOTES</span></span>

## <span data-ttu-id="8b6a3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b6a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b6a3-135">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b6a3-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="8b6a3-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b6a3-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="8b6a3-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b6a3-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


