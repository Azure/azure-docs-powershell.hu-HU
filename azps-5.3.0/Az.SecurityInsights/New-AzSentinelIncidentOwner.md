---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479708"
---
# <span data-ttu-id="f7302-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="f7302-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="f7302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7302-102">SYNOPSIS</span></span>
<span data-ttu-id="f7302-103">Az Incidens tulajdonosa objektum létrehozása az incidens tulajdonosának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f7302-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="f7302-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7302-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7302-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7302-105">DESCRIPTION</span></span>
<span data-ttu-id="f7302-106">A **New-AzSentinelIncidentOwner** parancsmag létrehoz egy Incidenstulajdonos objektumot a memóriában az incidens frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f7302-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="f7302-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7302-107">EXAMPLES</span></span>

### <span data-ttu-id="f7302-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7302-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="f7302-109">Ez a példa létrehoz egy **Incidenstulajdonost,** és frissíti az incidenst az új tulajdonosnak.</span><span class="sxs-lookup"><span data-stu-id="f7302-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="f7302-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7302-110">PARAMETERS</span></span>

### <span data-ttu-id="f7302-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="f7302-111">-AssignedTo</span></span>
<span data-ttu-id="f7302-112">Incidens tulajdonosa – Felelős</span><span class="sxs-lookup"><span data-stu-id="f7302-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="f7302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7302-113">-DefaultProfile</span></span>
<span data-ttu-id="f7302-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7302-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7302-115">-Email</span><span class="sxs-lookup"><span data-stu-id="f7302-115">-Email</span></span>
<span data-ttu-id="f7302-116">Incidens tulajdonosa – e-mail</span><span class="sxs-lookup"><span data-stu-id="f7302-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="f7302-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7302-117">-ObjectId</span></span>
<span data-ttu-id="f7302-118">Incidens tulajdonosa – ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7302-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="f7302-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f7302-119">-UserPrincipalName</span></span>
<span data-ttu-id="f7302-120">Incidens tulajdonosa – egyszerű felhasználónév</span><span class="sxs-lookup"><span data-stu-id="f7302-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="f7302-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7302-121">CommonParameters</span></span>
<span data-ttu-id="f7302-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7302-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7302-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7302-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7302-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7302-124">INPUTS</span></span>

### <span data-ttu-id="f7302-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7302-125">None</span></span>
## <span data-ttu-id="f7302-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7302-126">OUTPUTS</span></span>

### <span data-ttu-id="f7302-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f7302-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="f7302-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7302-128">NOTES</span></span>

## <span data-ttu-id="f7302-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7302-129">RELATED LINKS</span></span>
