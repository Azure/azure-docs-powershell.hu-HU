---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934154"
---
# <span data-ttu-id="8b778-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8b778-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="8b778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b778-102">SYNOPSIS</span></span>
<span data-ttu-id="8b778-103">Az aktuális hitelesített felhasználó vagy egyszerű szolgáltatásnév Microsoft Partner Network(MPN)-azonosítóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b778-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8b778-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b778-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b778-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b778-105">DESCRIPTION</span></span>
<span data-ttu-id="8b778-106">Az aktuális hitelesített felhasználó vagy egyszerű szolgáltatásnév Microsoft Partner Network(MPN)-azonosítóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b778-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8b778-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b778-107">EXAMPLES</span></span>

### <span data-ttu-id="8b778-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8b778-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="8b778-109">A jelenlegi felügyeleti partnerazonosító lekérte</span><span class="sxs-lookup"><span data-stu-id="8b778-109">Get the current management partner id</span></span>

### <span data-ttu-id="8b778-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="8b778-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="8b778-111">Szerezze be a jelenlegi felügyeleti partnerazonosítót egy partnerazonosító használatával, ha nem egyeznek, az nem fog sikerülni.</span><span class="sxs-lookup"><span data-stu-id="8b778-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="8b778-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b778-112">PARAMETERS</span></span>

### <span data-ttu-id="8b778-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b778-113">-DefaultProfile</span></span>
<span data-ttu-id="8b778-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b778-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b778-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="8b778-115">-PartnerId</span></span>
<span data-ttu-id="8b778-116">A vezető partner azonosítója, ez egy 6 jegyű szám.</span><span class="sxs-lookup"><span data-stu-id="8b778-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="8b778-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b778-117">CommonParameters</span></span>
<span data-ttu-id="8b778-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b778-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b778-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b778-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b778-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b778-120">INPUTS</span></span>

### <span data-ttu-id="8b778-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b778-121">None</span></span>

## <span data-ttu-id="8b778-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b778-122">OUTPUTS</span></span>

### <span data-ttu-id="8b778-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8b778-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="8b778-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b778-124">NOTES</span></span>

## <span data-ttu-id="8b778-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b778-125">RELATED LINKS</span></span>

[<span data-ttu-id="8b778-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8b778-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="8b778-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8b778-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="8b778-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8b778-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)