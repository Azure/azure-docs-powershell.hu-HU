---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195819"
---
# <span data-ttu-id="a5b55-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a5b55-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="a5b55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5b55-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b55-103">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a5b55-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a5b55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5b55-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5b55-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b55-106">Frissíti az aktuális hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a5b55-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a5b55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5b55-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b55-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a5b55-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="a5b55-109">A felügyeleti partner frissítése egy új webhelyre</span><span class="sxs-lookup"><span data-stu-id="a5b55-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="a5b55-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5b55-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b55-111">-DefaultProfile</span></span>
<span data-ttu-id="a5b55-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5b55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b55-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="a5b55-113">-PartnerId</span></span>
<span data-ttu-id="a5b55-114">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="a5b55-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="a5b55-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5b55-115">-Confirm</span></span>
<span data-ttu-id="a5b55-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5b55-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b55-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b55-117">-WhatIf</span></span>
<span data-ttu-id="a5b55-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5b55-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b55-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5b55-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b55-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b55-120">CommonParameters</span></span>
<span data-ttu-id="a5b55-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5b55-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b55-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b55-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b55-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5b55-123">INPUTS</span></span>

### <span data-ttu-id="a5b55-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5b55-124">None</span></span>

## <span data-ttu-id="a5b55-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5b55-125">OUTPUTS</span></span>

### <span data-ttu-id="a5b55-126">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a5b55-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="a5b55-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5b55-127">NOTES</span></span>

## <span data-ttu-id="a5b55-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5b55-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5b55-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a5b55-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="a5b55-130">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a5b55-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="a5b55-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a5b55-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)