---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195812"
---
# <span data-ttu-id="03244-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="03244-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="03244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03244-102">SYNOPSIS</span></span>
<span data-ttu-id="03244-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="03244-103">Regenerates an account key.</span></span>

## <span data-ttu-id="03244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03244-104">SYNTAX</span></span>

### <span data-ttu-id="03244-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03244-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03244-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03244-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03244-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03244-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03244-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="03244-108">DESCRIPTION</span></span>
<span data-ttu-id="03244-109">Az New-AzMapsAccountKey parancsmag újragenerálja az Azure Maps-fiók API-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="03244-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="03244-110">Példák</span><span class="sxs-lookup"><span data-stu-id="03244-110">EXAMPLES</span></span>

### <span data-ttu-id="03244-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03244-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="03244-112">Újragenerálja az elsődleges API-kulcsot az erőforráscsoport MyResourceGroup tartozó MyAccount.</span><span class="sxs-lookup"><span data-stu-id="03244-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="03244-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="03244-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="03244-114">Újragenerálja a megadott Azure Maps-fiók másodlagos API-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="03244-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="03244-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03244-115">PARAMETERS</span></span>

### <span data-ttu-id="03244-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03244-116">-DefaultProfile</span></span>
<span data-ttu-id="03244-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03244-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03244-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03244-118">-InputObject</span></span>
<span data-ttu-id="03244-119">A Get-AzMapsAccount átirányítja a fiókját.</span><span class="sxs-lookup"><span data-stu-id="03244-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03244-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="03244-120">-KeyName</span></span>
<span data-ttu-id="03244-121">A fiókok megfeleltetése gomb</span><span class="sxs-lookup"><span data-stu-id="03244-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03244-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03244-122">-Name</span></span>
<span data-ttu-id="03244-123">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="03244-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03244-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03244-124">-ResourceGroupName</span></span>
<span data-ttu-id="03244-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="03244-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03244-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03244-126">-ResourceId</span></span>
<span data-ttu-id="03244-127">Térképek fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="03244-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03244-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03244-128">-Confirm</span></span>
<span data-ttu-id="03244-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03244-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03244-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03244-130">-WhatIf</span></span>
<span data-ttu-id="03244-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03244-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03244-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03244-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03244-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03244-133">CommonParameters</span></span>
<span data-ttu-id="03244-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03244-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03244-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03244-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03244-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03244-136">INPUTS</span></span>

### <span data-ttu-id="03244-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03244-137">System.String</span></span>

### <span data-ttu-id="03244-138">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="03244-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="03244-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03244-139">OUTPUTS</span></span>

### <span data-ttu-id="03244-140">Microsoft. Azure. Management. maps. models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="03244-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="03244-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03244-141">NOTES</span></span>

## <span data-ttu-id="03244-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03244-142">RELATED LINKS</span></span>
