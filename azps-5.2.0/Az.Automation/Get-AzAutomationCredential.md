---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328408"
---
# <span data-ttu-id="2c25a-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c25a-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="2c25a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c25a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c25a-103">Automatizálási hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="2c25a-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="2c25a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c25a-104">SYNTAX</span></span>

### <span data-ttu-id="2c25a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c25a-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c25a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2c25a-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c25a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c25a-107">DESCRIPTION</span></span>
<span data-ttu-id="2c25a-108">A **Get-AzAutomationCredential** parancsmag egy vagy több Azure Automation-hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="2c25a-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="2c25a-109">A rendszer alapértelmezés szerint minden hitelesítő adatát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2c25a-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="2c25a-110">A hitelesítő adatok megadásához adja meg a hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="2c25a-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="2c25a-111">Biztonsági okokból ez a parancsmag nem ad vissza hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="2c25a-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="2c25a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c25a-112">EXAMPLES</span></span>

### <span data-ttu-id="2c25a-113">1. példa: Az összes hitelesítő adat lekérte</span><span class="sxs-lookup"><span data-stu-id="2c25a-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="2c25a-114">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes hitelesítő adatához.</span><span class="sxs-lookup"><span data-stu-id="2c25a-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2c25a-115">2. példa: Hitelesítő adatok lekérte</span><span class="sxs-lookup"><span data-stu-id="2c25a-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="2c25a-116">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoCredential nevű hitelesítő adatainak metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="2c25a-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2c25a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c25a-117">PARAMETERS</span></span>

### <span data-ttu-id="2c25a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c25a-118">-AutomationAccountName</span></span>
<span data-ttu-id="2c25a-119">Annak az automatizálási fióknak a nevét adja meg, amelyhez a parancsmag hitelesítő adatokat olvassa be.</span><span class="sxs-lookup"><span data-stu-id="2c25a-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="2c25a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c25a-120">-DefaultProfile</span></span>
<span data-ttu-id="2c25a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c25a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c25a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2c25a-122">-Name</span></span>
<span data-ttu-id="2c25a-123">A visszakeresni szükséges hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c25a-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="2c25a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c25a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c25a-125">Megadja azt az erőforráscsoportot, amelynek hitelesítő adatait a parancsmagja beolvassa.</span><span class="sxs-lookup"><span data-stu-id="2c25a-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="2c25a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c25a-126">CommonParameters</span></span>
<span data-ttu-id="2c25a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c25a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c25a-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c25a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c25a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c25a-129">INPUTS</span></span>

### <span data-ttu-id="2c25a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2c25a-130">System.String</span></span>

## <span data-ttu-id="2c25a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c25a-131">OUTPUTS</span></span>

### <span data-ttu-id="2c25a-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="2c25a-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="2c25a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c25a-133">NOTES</span></span>

## <span data-ttu-id="2c25a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c25a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2c25a-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c25a-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="2c25a-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c25a-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="2c25a-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c25a-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


