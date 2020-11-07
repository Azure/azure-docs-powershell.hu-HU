---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671480"
---
# <span data-ttu-id="68335-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="68335-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="68335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68335-102">SYNOPSIS</span></span>
<span data-ttu-id="68335-103">DSC csomópont eltávolítása a vezetőségtől automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="68335-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="68335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68335-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68335-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68335-105">DESCRIPTION</span></span>
<span data-ttu-id="68335-106">A **unregister-AzAutomationDscNode** parancsmag egy, az APS-hez szükséges állapot-konfigurációt (DSC) tartalmazó csomópontot távolít el a vezetőségtől egy Azure automatizálási fiókkal.</span><span class="sxs-lookup"><span data-stu-id="68335-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="68335-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68335-107">EXAMPLES</span></span>

### <span data-ttu-id="68335-108">1. példa: az Azure DSC csomópont eltávolítása a kezelésből automatizálási fiókból</span><span class="sxs-lookup"><span data-stu-id="68335-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="68335-109">Ez a parancs eltávolítja azt a DSC csomópontot, amely a Contoso17 nevű automatizálási fiók kezelésével rendelkezik a megadott GUID azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="68335-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="68335-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68335-110">PARAMETERS</span></span>

### <span data-ttu-id="68335-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68335-111">-AutomationAccountName</span></span>
<span data-ttu-id="68335-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a DSC csomópontot.</span><span class="sxs-lookup"><span data-stu-id="68335-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="68335-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68335-113">-DefaultProfile</span></span>
<span data-ttu-id="68335-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68335-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68335-115">-Force</span><span class="sxs-lookup"><span data-stu-id="68335-115">-Force</span></span>
<span data-ttu-id="68335-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="68335-116">ps_force</span></span>

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

### <span data-ttu-id="68335-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="68335-117">-Id</span></span>
<span data-ttu-id="68335-118">A parancsmag által eltávolított DSC csomópont egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="68335-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68335-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68335-119">-ResourceGroupName</span></span>
<span data-ttu-id="68335-120">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag egy DSC csomópontot beiktat.</span><span class="sxs-lookup"><span data-stu-id="68335-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="68335-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68335-121">-Confirm</span></span>
<span data-ttu-id="68335-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68335-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68335-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68335-123">-WhatIf</span></span>
<span data-ttu-id="68335-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68335-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68335-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68335-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68335-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68335-126">CommonParameters</span></span>
<span data-ttu-id="68335-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68335-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68335-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68335-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68335-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68335-129">INPUTS</span></span>

### <span data-ttu-id="68335-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="68335-130">System.Guid</span></span>

### <span data-ttu-id="68335-131">System. String</span><span class="sxs-lookup"><span data-stu-id="68335-131">System.String</span></span>

## <span data-ttu-id="68335-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68335-132">OUTPUTS</span></span>

### <span data-ttu-id="68335-133">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="68335-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="68335-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68335-134">NOTES</span></span>

## <span data-ttu-id="68335-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68335-135">RELATED LINKS</span></span>

[<span data-ttu-id="68335-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="68335-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="68335-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="68335-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="68335-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="68335-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


