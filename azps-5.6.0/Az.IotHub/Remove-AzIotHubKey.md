---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934361"
---
# <span data-ttu-id="55702-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="55702-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="55702-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55702-102">SYNOPSIS</span></span>
<span data-ttu-id="55702-103">Eltávolít egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="55702-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="55702-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55702-104">SYNTAX</span></span>

### <span data-ttu-id="55702-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55702-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55702-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55702-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55702-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55702-107">DESCRIPTION</span></span>
<span data-ttu-id="55702-108">Eltávolít egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="55702-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="55702-109">Ha több, azonos nevű kulcs van, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="55702-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="55702-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55702-110">EXAMPLES</span></span>

### <span data-ttu-id="55702-111">1. példa: IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="55702-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="55702-112">Eltávolítja az iothubowner1 nevű kulcsot a myiothub nevű IotHubból.</span><span class="sxs-lookup"><span data-stu-id="55702-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="55702-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55702-113">PARAMETERS</span></span>

### <span data-ttu-id="55702-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55702-114">-DefaultProfile</span></span>
<span data-ttu-id="55702-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="55702-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55702-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="55702-116">-HubId</span></span>
<span data-ttu-id="55702-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="55702-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55702-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="55702-118">-KeyName</span></span>
<span data-ttu-id="55702-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="55702-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55702-120">-Name</span><span class="sxs-lookup"><span data-stu-id="55702-120">-Name</span></span>
<span data-ttu-id="55702-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="55702-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55702-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55702-122">-ResourceGroupName</span></span>
<span data-ttu-id="55702-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="55702-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55702-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55702-124">-Confirm</span></span>
<span data-ttu-id="55702-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55702-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55702-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55702-126">-WhatIf</span></span>
<span data-ttu-id="55702-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55702-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55702-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55702-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55702-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55702-129">CommonParameters</span></span>
<span data-ttu-id="55702-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55702-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55702-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55702-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55702-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55702-132">INPUTS</span></span>

### <span data-ttu-id="55702-133">System.String</span><span class="sxs-lookup"><span data-stu-id="55702-133">System.String</span></span>

## <span data-ttu-id="55702-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55702-134">OUTPUTS</span></span>

### <span data-ttu-id="55702-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="55702-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="55702-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55702-136">NOTES</span></span>

## <span data-ttu-id="55702-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55702-137">RELATED LINKS</span></span>
