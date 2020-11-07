---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672178"
---
# <span data-ttu-id="7fbba-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7fbba-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="7fbba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fbba-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbba-103">Automatizálási hitelesítő adatok jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="7fbba-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fbba-104">SYNTAX</span></span>

### <span data-ttu-id="7fbba-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fbba-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fbba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7fbba-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fbba-107">DESCRIPTION</span></span>
<span data-ttu-id="7fbba-108">A **Get-AzureRmAutomationCredential** parancsmag egy vagy több Azure Automation hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="7fbba-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="7fbba-109">Alapértelmezés szerint minden hitelesítő adatot visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7fbba-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="7fbba-110">Adja meg a hitelesítő adatokhoz tartozó hitelesítő adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="7fbba-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="7fbba-111">Biztonsági okokból ez a parancsmag nem adja meg a hitelesítő adatok jelszavát.</span><span class="sxs-lookup"><span data-stu-id="7fbba-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="7fbba-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7fbba-112">EXAMPLES</span></span>

### <span data-ttu-id="7fbba-113">Példa 1: a hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="7fbba-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7fbba-114">Ez a parancs a Contoso17 nevű automatizálási fiók összes hitelesítő adatainak metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="7fbba-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7fbba-115">2. példa: hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="7fbba-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="7fbba-116">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoCredential nevű hitelesítő adatainak metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7fbba-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7fbba-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fbba-117">PARAMETERS</span></span>

### <span data-ttu-id="7fbba-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7fbba-118">-AutomationAccountName</span></span>
<span data-ttu-id="7fbba-119">Annak az automatizálási fióknak a neve, amelyhez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="7fbba-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="7fbba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbba-120">-DefaultProfile</span></span>
<span data-ttu-id="7fbba-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7fbba-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fbba-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7fbba-122">-Name</span></span>
<span data-ttu-id="7fbba-123">A lekérdezni kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fbba-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbba-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fbba-125">Azt az erőforráscsoportot adja meg, amelyhez ez a parancsmag a hitelesítő adatokat kéri.</span><span class="sxs-lookup"><span data-stu-id="7fbba-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="7fbba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbba-126">CommonParameters</span></span>
<span data-ttu-id="7fbba-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fbba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbba-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbba-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fbba-129">INPUTS</span></span>

### <span data-ttu-id="7fbba-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="7fbba-130">None</span></span>
<span data-ttu-id="7fbba-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7fbba-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7fbba-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fbba-132">OUTPUTS</span></span>

### <span data-ttu-id="7fbba-133">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="7fbba-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="7fbba-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fbba-134">NOTES</span></span>

## <span data-ttu-id="7fbba-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fbba-135">RELATED LINKS</span></span>

[<span data-ttu-id="7fbba-136">Új – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7fbba-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="7fbba-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7fbba-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="7fbba-138">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7fbba-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


