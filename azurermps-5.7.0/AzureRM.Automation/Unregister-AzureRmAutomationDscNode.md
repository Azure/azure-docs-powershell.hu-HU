---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 486664833e585733dc02a5c6f1c94d8673dfc4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501531"
---
# <span data-ttu-id="f79cd-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f79cd-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="f79cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f79cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f79cd-103">DSC csomópont eltávolítása a vezetőségtől automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="f79cd-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f79cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f79cd-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f79cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f79cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f79cd-106">A **unregister-AzureRmAutomationDscNode** parancsmag egy, az APS-hez szükséges állapot-konfigurációt (DSC) tartalmazó csomópontot távolít el a vezetőségtől egy Azure automatizálási fiókkal.</span><span class="sxs-lookup"><span data-stu-id="f79cd-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="f79cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f79cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f79cd-108">1. példa: az Azure DSC csomópont eltávolítása a kezelésből automatizálási fiókból</span><span class="sxs-lookup"><span data-stu-id="f79cd-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="f79cd-109">Ez a parancs eltávolítja azt a DSC csomópontot, amely a Contoso17 nevű automatizálási fiók kezelésével rendelkezik a megadott GUID azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="f79cd-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f79cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f79cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f79cd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f79cd-111">-AutomationAccountName</span></span>
<span data-ttu-id="f79cd-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a DSC csomópontot.</span><span class="sxs-lookup"><span data-stu-id="f79cd-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="f79cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79cd-113">-DefaultProfile</span></span>
<span data-ttu-id="f79cd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f79cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f79cd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f79cd-115">-Force</span></span>
<span data-ttu-id="f79cd-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="f79cd-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79cd-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f79cd-117">-Id</span></span>
<span data-ttu-id="f79cd-118">A parancsmag által eltávolított DSC csomópont egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f79cd-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="f79cd-120">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag egy DSC csomópontot beiktat.</span><span class="sxs-lookup"><span data-stu-id="f79cd-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="f79cd-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f79cd-121">-Confirm</span></span>
<span data-ttu-id="f79cd-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f79cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79cd-123">-WhatIf</span></span>
<span data-ttu-id="f79cd-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f79cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f79cd-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f79cd-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79cd-126">CommonParameters</span></span>
<span data-ttu-id="f79cd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f79cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79cd-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79cd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f79cd-129">INPUTS</span></span>

### <span data-ttu-id="f79cd-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="f79cd-130">None</span></span>
<span data-ttu-id="f79cd-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f79cd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f79cd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f79cd-132">OUTPUTS</span></span>

### <span data-ttu-id="f79cd-133">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="f79cd-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="f79cd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f79cd-134">NOTES</span></span>

## <span data-ttu-id="f79cd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f79cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="f79cd-136">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f79cd-136">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="f79cd-137">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f79cd-137">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="f79cd-138">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f79cd-138">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


