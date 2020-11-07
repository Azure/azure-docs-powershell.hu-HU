---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667802"
---
# <span data-ttu-id="a28ca-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="a28ca-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="a28ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a28ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a28ca-103">Automatizálja a regisztrációs kulcsokat egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a28ca-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="a28ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a28ca-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a28ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a28ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a28ca-106">A **New-AzAutomationKey** parancsmag újragenerálja a regisztrációs kulcsokat az Azure automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a28ca-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="a28ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a28ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a28ca-108">1. példa: egy automatizálási fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="a28ca-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a28ca-109">Ez a parancs újra létrehozta a AutomationAccount01 nevű Azure Automation fiók elsődleges kulcsát a ResourceGroup01 nevű erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="a28ca-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a28ca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a28ca-110">PARAMETERS</span></span>

### <span data-ttu-id="a28ca-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a28ca-111">-AutomationAccountName</span></span>
<span data-ttu-id="a28ca-112">Annak az automatizálási fióknak a nevét adja meg, amelyre a parancsmag újragenerálja a kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="a28ca-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="a28ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28ca-113">-DefaultProfile</span></span>
<span data-ttu-id="a28ca-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a28ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a28ca-115">-Típus</span><span class="sxs-lookup"><span data-stu-id="a28ca-115">-KeyType</span></span>
<span data-ttu-id="a28ca-116">Az ügynök regisztrációs kulcsának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a28ca-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="a28ca-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a28ca-117">Valid values are:</span></span> 
- <span data-ttu-id="a28ca-118">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="a28ca-118">Primary</span></span> 
- <span data-ttu-id="a28ca-119">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="a28ca-119">Secondary</span></span>

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

### <span data-ttu-id="a28ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="a28ca-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a28ca-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a28ca-122">Ez a parancsmag újragenerálja az automatizálási fiók kulcsait abban az erőforráscsoport-ban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a28ca-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a28ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28ca-123">CommonParameters</span></span>
<span data-ttu-id="a28ca-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a28ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28ca-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28ca-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28ca-126">INPUTS</span></span>

### <span data-ttu-id="a28ca-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a28ca-127">System.String</span></span>

## <span data-ttu-id="a28ca-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28ca-128">OUTPUTS</span></span>

### <span data-ttu-id="a28ca-129">Microsoft. Azure. Command. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="a28ca-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="a28ca-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a28ca-130">NOTES</span></span>

## <span data-ttu-id="a28ca-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a28ca-131">RELATED LINKS</span></span>
