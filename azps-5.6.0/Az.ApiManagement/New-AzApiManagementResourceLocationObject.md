---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 88b2ae64430f73df242d7003baa2c72ec6512dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923865"
---
# <span data-ttu-id="e7947-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="e7947-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="e7947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7947-102">SYNOPSIS</span></span>
<span data-ttu-id="e7947-103">Új erőforráshely-szerződés létrehozása (az átjárókban használatos).</span><span class="sxs-lookup"><span data-stu-id="e7947-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e7947-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7947-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7947-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7947-105">DESCRIPTION</span></span>
<span data-ttu-id="e7947-106">A **New-AzApiManagementResourceLocationObject** parancsmag létrehoz egy új erőforráshely-szerződést (az átjárókban használatos).</span><span class="sxs-lookup"><span data-stu-id="e7947-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e7947-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7947-107">EXAMPLES</span></span>

### <span data-ttu-id="e7947-108">1. példa: Erőforrás-helyszerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7947-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="e7947-109">Ez a parancs létrehoz egy erőforráshelyet.</span><span class="sxs-lookup"><span data-stu-id="e7947-109">This command creates a resource location.</span></span>

## <span data-ttu-id="e7947-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7947-110">PARAMETERS</span></span>

### <span data-ttu-id="e7947-111">-City</span><span class="sxs-lookup"><span data-stu-id="e7947-111">-City</span></span>
<span data-ttu-id="e7947-112">Location City (Település) adatokat.</span><span class="sxs-lookup"><span data-stu-id="e7947-112">Location City.</span></span>
<span data-ttu-id="e7947-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e7947-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7947-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e7947-114">-CountryOrRegion</span></span>
<span data-ttu-id="e7947-115">Hely országa vagy régiója.</span><span class="sxs-lookup"><span data-stu-id="e7947-115">Location Country or Region.</span></span>
<span data-ttu-id="e7947-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e7947-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7947-117">-DefaultProfile</span></span>
<span data-ttu-id="e7947-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7947-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7947-119">-District</span><span class="sxs-lookup"><span data-stu-id="e7947-119">-District</span></span>
<span data-ttu-id="e7947-120">Hely körzete.</span><span class="sxs-lookup"><span data-stu-id="e7947-120">Location District.</span></span>
<span data-ttu-id="e7947-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e7947-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7947-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e7947-122">-Name</span></span>
<span data-ttu-id="e7947-123">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="e7947-123">Location Name.</span></span>
<span data-ttu-id="e7947-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e7947-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7947-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7947-125">CommonParameters</span></span>
<span data-ttu-id="e7947-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7947-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7947-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7947-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7947-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7947-128">INPUTS</span></span>

### <span data-ttu-id="e7947-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7947-129">None</span></span>

## <span data-ttu-id="e7947-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7947-130">OUTPUTS</span></span>

### <span data-ttu-id="e7947-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="e7947-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e7947-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7947-132">NOTES</span></span>

## <span data-ttu-id="e7947-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7947-133">RELATED LINKS</span></span>
