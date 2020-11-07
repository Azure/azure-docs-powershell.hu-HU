---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679982"
---
# <span data-ttu-id="a6378-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a6378-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="a6378-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6378-102">SYNOPSIS</span></span>
<span data-ttu-id="a6378-103">DSC csomópont eltávolítása a vezetőségtől automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="a6378-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6378-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6378-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6378-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6378-105">DESCRIPTION</span></span>
<span data-ttu-id="a6378-106">A **unregister-AzureRmAutomationDscNode** parancsmag egy, az APS-hez szükséges állapot-konfigurációt (DSC) tartalmazó csomópontot távolít el a vezetőségtől egy Azure automatizálási fiókkal.</span><span class="sxs-lookup"><span data-stu-id="a6378-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="a6378-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6378-107">EXAMPLES</span></span>

### <span data-ttu-id="a6378-108">1. példa: az Azure DSC csomópont eltávolítása a kezelésből automatizálási fiókból</span><span class="sxs-lookup"><span data-stu-id="a6378-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="a6378-109">Ez a parancs eltávolítja azt a DSC csomópontot, amely a Contoso17 nevű automatizálási fiók kezelésével rendelkezik a megadott GUID azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="a6378-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a6378-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6378-110">PARAMETERS</span></span>

### <span data-ttu-id="a6378-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6378-111">-AutomationAccountName</span></span>
<span data-ttu-id="a6378-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a DSC csomópontot.</span><span class="sxs-lookup"><span data-stu-id="a6378-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="a6378-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a6378-113">-Force</span></span>
<span data-ttu-id="a6378-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="a6378-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6378-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a6378-115">-Id</span></span>
<span data-ttu-id="a6378-116">A parancsmag által eltávolított DSC csomópont egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6378-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6378-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6378-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6378-118">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag egy DSC csomópontot beiktat.</span><span class="sxs-lookup"><span data-stu-id="a6378-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="a6378-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6378-119">-Confirm</span></span>
<span data-ttu-id="a6378-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6378-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6378-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6378-121">-WhatIf</span></span>
<span data-ttu-id="a6378-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6378-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6378-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6378-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6378-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6378-124">-DefaultProfile</span></span>
<span data-ttu-id="a6378-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6378-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6378-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6378-126">CommonParameters</span></span>
<span data-ttu-id="a6378-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6378-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6378-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6378-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6378-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6378-129">INPUTS</span></span>

## <span data-ttu-id="a6378-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6378-130">OUTPUTS</span></span>

### <span data-ttu-id="a6378-131">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="a6378-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="a6378-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6378-132">NOTES</span></span>

## <span data-ttu-id="a6378-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6378-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6378-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a6378-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a6378-135">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a6378-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a6378-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a6378-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


