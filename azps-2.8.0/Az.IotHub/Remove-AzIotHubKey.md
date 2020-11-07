---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: eb0ec4390cb8e354707109ecafb5d284b70fa910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666245"
---
# <span data-ttu-id="b9a72-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b9a72-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="b9a72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9a72-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a72-103">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b9a72-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="b9a72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9a72-104">SYNTAX</span></span>

### <span data-ttu-id="b9a72-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9a72-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a72-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9a72-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a72-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9a72-107">DESCRIPTION</span></span>
<span data-ttu-id="b9a72-108">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b9a72-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="b9a72-109">Ha több olyan billentyű is létezik, amely ugyanazt a nevet adja, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="b9a72-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="b9a72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9a72-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a72-111">Példa 1 IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="b9a72-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="b9a72-112">A "myiothub" nevű IotHub eltávolítja a iothubowner1 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b9a72-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b9a72-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9a72-113">PARAMETERS</span></span>

### <span data-ttu-id="b9a72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a72-114">-DefaultProfile</span></span>
<span data-ttu-id="b9a72-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9a72-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9a72-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="b9a72-116">-HubId</span></span>
<span data-ttu-id="b9a72-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b9a72-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b9a72-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="b9a72-118">-KeyName</span></span>
<span data-ttu-id="b9a72-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="b9a72-119">Name of the Key</span></span>

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

### <span data-ttu-id="b9a72-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9a72-120">-Name</span></span>
<span data-ttu-id="b9a72-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="b9a72-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b9a72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a72-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9a72-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b9a72-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b9a72-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9a72-124">-Confirm</span></span>
<span data-ttu-id="b9a72-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9a72-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a72-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a72-126">-WhatIf</span></span>
<span data-ttu-id="b9a72-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9a72-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a72-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9a72-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a72-129">CommonParameters</span></span>
<span data-ttu-id="b9a72-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9a72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a72-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a72-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a72-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9a72-132">INPUTS</span></span>

### <span data-ttu-id="b9a72-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a72-133">System.String</span></span>

## <span data-ttu-id="b9a72-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9a72-134">OUTPUTS</span></span>

### <span data-ttu-id="b9a72-135">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b9a72-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b9a72-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9a72-136">NOTES</span></span>

## <span data-ttu-id="b9a72-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9a72-137">RELATED LINKS</span></span>
