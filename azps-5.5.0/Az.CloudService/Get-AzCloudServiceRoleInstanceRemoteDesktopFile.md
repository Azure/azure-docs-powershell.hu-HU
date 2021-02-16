---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149027"
---
# <span data-ttu-id="18100-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="18100-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="18100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18100-102">SYNOPSIS</span></span>
<span data-ttu-id="18100-103">Távoli asztali fájlt kap egy szerepkörpéldányhoz egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="18100-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="18100-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18100-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="18100-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18100-105">DESCRIPTION</span></span>
<span data-ttu-id="18100-106">Távoli asztali fájlt kap egy szerepkörpéldányhoz egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="18100-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="18100-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18100-107">EXAMPLES</span></span>

### <span data-ttu-id="18100-108">1. példa: RDP-fájl létrehozása</span><span class="sxs-lookup"><span data-stu-id="18100-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="18100-109">Ez a parancs egy RDP-fájlt kap a ContosoFrontEnd IN 0 nevű felhőszolgáltatáshoz( ContosoCS), amely a \_ ContosOrg nevű erőforráscsoporthoz \_ tartozik.</span><span class="sxs-lookup"><span data-stu-id="18100-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="18100-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18100-110">PARAMETERS</span></span>

### <span data-ttu-id="18100-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="18100-111">-CloudServiceName</span></span>
<span data-ttu-id="18100-112">.</span><span class="sxs-lookup"><span data-stu-id="18100-112">.</span></span>

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

### <span data-ttu-id="18100-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18100-113">-DefaultProfile</span></span>
<span data-ttu-id="18100-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18100-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18100-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="18100-115">-OutFile</span></span>
<span data-ttu-id="18100-116">Path to write output file to</span><span class="sxs-lookup"><span data-stu-id="18100-116">Path to write output file to</span></span>

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

### <span data-ttu-id="18100-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18100-117">-PassThru</span></span>
<span data-ttu-id="18100-118">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="18100-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="18100-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18100-119">-ResourceGroupName</span></span>
<span data-ttu-id="18100-120">.</span><span class="sxs-lookup"><span data-stu-id="18100-120">.</span></span>

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

### <span data-ttu-id="18100-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="18100-121">-RoleInstanceName</span></span>
<span data-ttu-id="18100-122">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="18100-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="18100-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18100-123">-SubscriptionId</span></span>
<span data-ttu-id="18100-124">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="18100-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18100-125">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="18100-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18100-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18100-126">CommonParameters</span></span>
<span data-ttu-id="18100-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18100-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18100-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18100-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18100-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18100-129">INPUTS</span></span>

## <span data-ttu-id="18100-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18100-130">OUTPUTS</span></span>

### <span data-ttu-id="18100-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18100-131">System.Boolean</span></span>

## <span data-ttu-id="18100-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18100-132">NOTES</span></span>

<span data-ttu-id="18100-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="18100-133">ALIASES</span></span>

## <span data-ttu-id="18100-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18100-134">RELATED LINKS</span></span>

