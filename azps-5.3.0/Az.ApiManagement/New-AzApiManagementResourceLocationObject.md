---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382421"
---
# <span data-ttu-id="e02f9-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="e02f9-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="e02f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e02f9-103">Új erőforráshely-szerződés létrehozása (az átjárókban használatos).</span><span class="sxs-lookup"><span data-stu-id="e02f9-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e02f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e02f9-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02f9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e02f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e02f9-106">A **New-AzApiManagementResourceLocationObject** parancsmag létrehoz egy új erőforráshely-szerződést (ezt az átjárók használják).</span><span class="sxs-lookup"><span data-stu-id="e02f9-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e02f9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e02f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e02f9-108">1. példa: Erőforrás-helyszerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="e02f9-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="e02f9-109">Ez a parancs létrehoz egy erőforráshelyet.</span><span class="sxs-lookup"><span data-stu-id="e02f9-109">This command creates a resource location.</span></span>

## <span data-ttu-id="e02f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e02f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e02f9-111">-City</span><span class="sxs-lookup"><span data-stu-id="e02f9-111">-City</span></span>
<span data-ttu-id="e02f9-112">Location City (Település) adatokat.</span><span class="sxs-lookup"><span data-stu-id="e02f9-112">Location City.</span></span>
<span data-ttu-id="e02f9-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e02f9-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="e02f9-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e02f9-114">-CountryOrRegion</span></span>
<span data-ttu-id="e02f9-115">Hely országa vagy régiója.</span><span class="sxs-lookup"><span data-stu-id="e02f9-115">Location Country or Region.</span></span>
<span data-ttu-id="e02f9-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e02f9-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e02f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02f9-117">-DefaultProfile</span></span>
<span data-ttu-id="e02f9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e02f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02f9-119">-District</span><span class="sxs-lookup"><span data-stu-id="e02f9-119">-District</span></span>
<span data-ttu-id="e02f9-120">Hely körzete.</span><span class="sxs-lookup"><span data-stu-id="e02f9-120">Location District.</span></span>
<span data-ttu-id="e02f9-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e02f9-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="e02f9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e02f9-122">-Name</span></span>
<span data-ttu-id="e02f9-123">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="e02f9-123">Location Name.</span></span>
<span data-ttu-id="e02f9-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e02f9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="e02f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02f9-125">CommonParameters</span></span>
<span data-ttu-id="e02f9-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02f9-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e02f9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02f9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e02f9-128">INPUTS</span></span>

### <span data-ttu-id="e02f9-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="e02f9-129">None</span></span>

## <span data-ttu-id="e02f9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e02f9-130">OUTPUTS</span></span>

### <span data-ttu-id="e02f9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="e02f9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e02f9-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e02f9-132">NOTES</span></span>

## <span data-ttu-id="e02f9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e02f9-133">RELATED LINKS</span></span>
