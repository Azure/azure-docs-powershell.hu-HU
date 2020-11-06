---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 0f8cbf67af4cc62c5cdeaae216a2c0a63cbe5afc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504603"
---
# <span data-ttu-id="639eb-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="639eb-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="639eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="639eb-102">SYNOPSIS</span></span>
<span data-ttu-id="639eb-103">Automatizálja a regisztrációs kulcsokat egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="639eb-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="639eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="639eb-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="639eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="639eb-105">DESCRIPTION</span></span>
<span data-ttu-id="639eb-106">A **New-AzureRmAutomationKey** parancsmag újragenerálja a regisztrációs kulcsokat az Azure automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="639eb-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="639eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="639eb-107">EXAMPLES</span></span>

### <span data-ttu-id="639eb-108">1. példa: egy automatizálási fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="639eb-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="639eb-109">Ez a parancs újra létrehozta a AutomationAccount01 nevű Azure Automation fiók elsődleges kulcsát a ResourceGroup01 nevű erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="639eb-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="639eb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="639eb-110">PARAMETERS</span></span>

### <span data-ttu-id="639eb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="639eb-111">-AutomationAccountName</span></span>
<span data-ttu-id="639eb-112">Annak az automatizálási fióknak a nevét adja meg, amelyre a parancsmag újragenerálja a kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="639eb-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="639eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639eb-113">-DefaultProfile</span></span>
<span data-ttu-id="639eb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="639eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="639eb-115">-Típus</span><span class="sxs-lookup"><span data-stu-id="639eb-115">-KeyType</span></span>
<span data-ttu-id="639eb-116">Az ügynök regisztrációs kulcsának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="639eb-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="639eb-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="639eb-117">Valid values are:</span></span> 

- <span data-ttu-id="639eb-118">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="639eb-118">Primary</span></span> 
- <span data-ttu-id="639eb-119">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="639eb-119">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="639eb-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="639eb-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="639eb-122">Ez a parancsmag újragenerálja az automatizálási fiók kulcsait abban az erőforráscsoport-ban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="639eb-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="639eb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639eb-123">CommonParameters</span></span>
<span data-ttu-id="639eb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="639eb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639eb-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639eb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639eb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="639eb-126">INPUTS</span></span>

### <span data-ttu-id="639eb-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="639eb-127">None</span></span>
<span data-ttu-id="639eb-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="639eb-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="639eb-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="639eb-129">OUTPUTS</span></span>

### <span data-ttu-id="639eb-130">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="639eb-130">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="639eb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="639eb-131">NOTES</span></span>

## <span data-ttu-id="639eb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="639eb-132">RELATED LINKS</span></span>

