---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368183"
---
# <span data-ttu-id="b8b7d-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8b7d-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="b8b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b7d-103">Egy Microsoft Partner Network(MPN) azonosítót társít az aktuálisan hitelesített felhasználóhoz vagy szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b8b7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8b7d-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8b7d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b7d-106">Egy Microsoft Partner Network(MPN) azonosítót társít az aktuálisan hitelesített felhasználóhoz vagy szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b8b7d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b7d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b8b7d-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b8b7d-109">Felügyeleti partner hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b8b7d-109">Add a management partner</span></span>

## <span data-ttu-id="b8b7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b7d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8b7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b7d-111">-DefaultProfile</span></span>
<span data-ttu-id="b8b7d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b7d-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b8b7d-113">-PartnerId</span></span>
<span data-ttu-id="b8b7d-114">A vezető partner azonosítója, ez egy 6 jegyű szám.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b7d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8b7d-115">-Confirm</span></span>
<span data-ttu-id="b8b7d-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b7d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b7d-117">-WhatIf</span></span>
<span data-ttu-id="b8b7d-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b7d-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b7d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b7d-120">CommonParameters</span></span>
<span data-ttu-id="b8b7d-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b7d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b7d-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b7d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b7d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8b7d-123">INPUTS</span></span>

### <span data-ttu-id="b8b7d-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b8b7d-124">None</span></span>

## <span data-ttu-id="b8b7d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8b7d-125">OUTPUTS</span></span>

### <span data-ttu-id="b8b7d-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8b7d-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b8b7d-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8b7d-127">NOTES</span></span>

## <span data-ttu-id="b8b7d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8b7d-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8b7d-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8b7d-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="b8b7d-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8b7d-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="b8b7d-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8b7d-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)