---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187329"
---
# <span data-ttu-id="3ca1a-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ca1a-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="3ca1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ca1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca1a-103">Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3ca1a-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3ca1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ca1a-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ca1a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ca1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca1a-106">Az aktuálisan hitelesített felhasználó vagy szolgáltatási megbízó Microsoft Partner Network (MPN) azonosítójának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3ca1a-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3ca1a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ca1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ca1a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ca1a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="3ca1a-109">A jelenlegi felügyeleti partner azonosítójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ca1a-109">Get the current management partner id</span></span>

### <span data-ttu-id="3ca1a-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="3ca1a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="3ca1a-111">A jelenlegi kezelési partnerek azonosítójának beszerzése partner-azonosítóval (ha nem egyeznek meg), sikertelen lesz</span><span class="sxs-lookup"><span data-stu-id="3ca1a-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="3ca1a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ca1a-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca1a-113">-DefaultProfile</span></span>
<span data-ttu-id="3ca1a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ca1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca1a-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="3ca1a-115">-PartnerId</span></span>
<span data-ttu-id="3ca1a-116">A kezelési partner azonosítója a 6 jegyű szám</span><span class="sxs-lookup"><span data-stu-id="3ca1a-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca1a-117">CommonParameters</span></span>
<span data-ttu-id="3ca1a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ca1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca1a-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca1a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca1a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca1a-120">INPUTS</span></span>

### <span data-ttu-id="3ca1a-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="3ca1a-121">None</span></span>

## <span data-ttu-id="3ca1a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca1a-122">OUTPUTS</span></span>

### <span data-ttu-id="3ca1a-123">Microsoft. Azure. Command. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ca1a-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="3ca1a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ca1a-124">NOTES</span></span>

## <span data-ttu-id="3ca1a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ca1a-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ca1a-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ca1a-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="3ca1a-127">Új – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ca1a-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="3ca1a-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ca1a-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)