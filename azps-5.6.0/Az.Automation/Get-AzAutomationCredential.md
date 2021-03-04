---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: f10bd8d57cd70004ed37f16234aa72dd3a1a8ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939769"
---
# <span data-ttu-id="a996d-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a996d-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="a996d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a996d-102">SYNOPSIS</span></span>
<span data-ttu-id="a996d-103">Automatizálási hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="a996d-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="a996d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a996d-104">SYNTAX</span></span>

### <span data-ttu-id="a996d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a996d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a996d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a996d-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a996d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a996d-107">DESCRIPTION</span></span>
<span data-ttu-id="a996d-108">A **Get-AzAutomationCredential** parancsmag egy vagy több Azure Automation-hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="a996d-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="a996d-109">A rendszer alapértelmezés szerint minden hitelesítő adatát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a996d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="a996d-110">A hitelesítő adatok megadásához adja meg a hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="a996d-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="a996d-111">Biztonsági okokból ez a parancsmag nem ad vissza hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a996d-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="a996d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a996d-112">EXAMPLES</span></span>

### <span data-ttu-id="a996d-113">1. példa: Az összes hitelesítő adat lekérte</span><span class="sxs-lookup"><span data-stu-id="a996d-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a996d-114">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes hitelesítő adatához.</span><span class="sxs-lookup"><span data-stu-id="a996d-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a996d-115">2. példa: Hitelesítő adatok lekérte</span><span class="sxs-lookup"><span data-stu-id="a996d-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="a996d-116">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoCredential nevű hitelesítő adatainak metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="a996d-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a996d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a996d-117">PARAMETERS</span></span>

### <span data-ttu-id="a996d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a996d-118">-AutomationAccountName</span></span>
<span data-ttu-id="a996d-119">Annak az automatizálási fióknak a nevét adja meg, amelyhez a parancsmag hitelesítő adatokat olvassa be.</span><span class="sxs-lookup"><span data-stu-id="a996d-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="a996d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a996d-120">-DefaultProfile</span></span>
<span data-ttu-id="a996d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a996d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a996d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a996d-122">-Name</span></span>
<span data-ttu-id="a996d-123">A visszakeresni szükséges hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a996d-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="a996d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a996d-124">-ResourceGroupName</span></span>
<span data-ttu-id="a996d-125">Megadja azt az erőforráscsoportot, amelynek hitelesítő adatait a parancsmagja beolvassa.</span><span class="sxs-lookup"><span data-stu-id="a996d-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="a996d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a996d-126">CommonParameters</span></span>
<span data-ttu-id="a996d-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a996d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a996d-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a996d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a996d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a996d-129">INPUTS</span></span>

### <span data-ttu-id="a996d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a996d-130">System.String</span></span>

## <span data-ttu-id="a996d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a996d-131">OUTPUTS</span></span>

### <span data-ttu-id="a996d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="a996d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="a996d-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a996d-133">NOTES</span></span>

## <span data-ttu-id="a996d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a996d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a996d-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a996d-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="a996d-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a996d-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="a996d-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a996d-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


