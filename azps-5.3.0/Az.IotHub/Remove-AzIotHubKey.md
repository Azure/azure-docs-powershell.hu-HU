---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386691"
---
# <span data-ttu-id="899f6-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="899f6-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="899f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899f6-102">SYNOPSIS</span></span>
<span data-ttu-id="899f6-103">Eltávolít egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="899f6-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="899f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="899f6-104">SYNTAX</span></span>

### <span data-ttu-id="899f6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="899f6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="899f6-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="899f6-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="899f6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="899f6-107">DESCRIPTION</span></span>
<span data-ttu-id="899f6-108">Eltávolít egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="899f6-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="899f6-109">Ha több, azonos nevű kulcs van, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="899f6-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="899f6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="899f6-110">EXAMPLES</span></span>

### <span data-ttu-id="899f6-111">1. példa: IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="899f6-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="899f6-112">Eltávolítja az iothubowner1 nevű kulcsot a myiothub nevű IotHubból.</span><span class="sxs-lookup"><span data-stu-id="899f6-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="899f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="899f6-113">PARAMETERS</span></span>

### <span data-ttu-id="899f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899f6-114">-DefaultProfile</span></span>
<span data-ttu-id="899f6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="899f6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="899f6-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="899f6-116">-HubId</span></span>
<span data-ttu-id="899f6-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="899f6-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="899f6-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="899f6-118">-KeyName</span></span>
<span data-ttu-id="899f6-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="899f6-119">Name of the Key</span></span>

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

### <span data-ttu-id="899f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="899f6-120">-Name</span></span>
<span data-ttu-id="899f6-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="899f6-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="899f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="899f6-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="899f6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="899f6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="899f6-124">-Confirm</span></span>
<span data-ttu-id="899f6-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="899f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899f6-126">-WhatIf</span></span>
<span data-ttu-id="899f6-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="899f6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899f6-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="899f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="899f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899f6-129">CommonParameters</span></span>
<span data-ttu-id="899f6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899f6-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899f6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899f6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="899f6-132">INPUTS</span></span>

### <span data-ttu-id="899f6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="899f6-133">System.String</span></span>

## <span data-ttu-id="899f6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="899f6-134">OUTPUTS</span></span>

### <span data-ttu-id="899f6-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="899f6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="899f6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="899f6-136">NOTES</span></span>

## <span data-ttu-id="899f6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="899f6-137">RELATED LINKS</span></span>
