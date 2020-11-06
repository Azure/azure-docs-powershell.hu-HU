---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503279"
---
# <span data-ttu-id="3f98e-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="3f98e-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="3f98e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f98e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f98e-103">Automatizálja a regisztrációs kulcsokat egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3f98e-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f98e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f98e-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f98e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f98e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f98e-106">A **New-AzureRmAutomationKey** parancsmag újragenerálja a regisztrációs kulcsokat az Azure automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3f98e-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="3f98e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f98e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f98e-108">1. példa: egy automatizálási fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="3f98e-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3f98e-109">Ez a parancs újra létrehozta a AutomationAccount01 nevű Azure Automation fiók elsődleges kulcsát a ResourceGroup01 nevű erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="3f98e-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3f98e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f98e-110">PARAMETERS</span></span>

### <span data-ttu-id="3f98e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f98e-111">-AutomationAccountName</span></span>
<span data-ttu-id="3f98e-112">Annak az automatizálási fióknak a nevét adja meg, amelyre a parancsmag újragenerálja a kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="3f98e-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="3f98e-113">-Típus</span><span class="sxs-lookup"><span data-stu-id="3f98e-113">-KeyType</span></span>
<span data-ttu-id="3f98e-114">Az ügynök regisztrációs kulcsának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f98e-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="3f98e-115">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3f98e-115">Valid values are:</span></span> 

- <span data-ttu-id="3f98e-116">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="3f98e-116">Primary</span></span> 
- <span data-ttu-id="3f98e-117">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="3f98e-117">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f98e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f98e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f98e-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f98e-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f98e-120">Ez a parancsmag újragenerálja az automatizálási fiók kulcsait abban az erőforráscsoport-ban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3f98e-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f98e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f98e-121">-DefaultProfile</span></span>
<span data-ttu-id="3f98e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f98e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f98e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f98e-123">CommonParameters</span></span>
<span data-ttu-id="3f98e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f98e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f98e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f98e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f98e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f98e-126">INPUTS</span></span>

## <span data-ttu-id="3f98e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f98e-127">OUTPUTS</span></span>

### <span data-ttu-id="3f98e-128">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="3f98e-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="3f98e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f98e-129">NOTES</span></span>

## <span data-ttu-id="3f98e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f98e-130">RELATED LINKS</span></span>

