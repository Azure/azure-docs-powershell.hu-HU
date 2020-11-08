---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185323"
---
# <span data-ttu-id="662e0-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="662e0-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="662e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="662e0-102">SYNOPSIS</span></span>
<span data-ttu-id="662e0-103">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="662e0-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="662e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="662e0-104">SYNTAX</span></span>

### <span data-ttu-id="662e0-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="662e0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662e0-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="662e0-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="662e0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="662e0-107">DESCRIPTION</span></span>
<span data-ttu-id="662e0-108">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="662e0-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="662e0-109">Ha több olyan billentyű is létezik, amely ugyanazt a nevet adja, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="662e0-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="662e0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="662e0-110">EXAMPLES</span></span>

### <span data-ttu-id="662e0-111">Példa 1 IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="662e0-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="662e0-112">A "myiothub" nevű IotHub eltávolítja a iothubowner1 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="662e0-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="662e0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="662e0-113">PARAMETERS</span></span>

### <span data-ttu-id="662e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662e0-114">-DefaultProfile</span></span>
<span data-ttu-id="662e0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="662e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="662e0-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="662e0-116">-HubId</span></span>
<span data-ttu-id="662e0-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="662e0-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="662e0-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="662e0-118">-KeyName</span></span>
<span data-ttu-id="662e0-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="662e0-119">Name of the Key</span></span>

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

### <span data-ttu-id="662e0-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="662e0-120">-Name</span></span>
<span data-ttu-id="662e0-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="662e0-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="662e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="662e0-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="662e0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="662e0-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="662e0-124">-Confirm</span></span>
<span data-ttu-id="662e0-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="662e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662e0-126">-WhatIf</span></span>
<span data-ttu-id="662e0-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="662e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="662e0-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="662e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="662e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662e0-129">CommonParameters</span></span>
<span data-ttu-id="662e0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="662e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662e0-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="662e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662e0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="662e0-132">INPUTS</span></span>

### <span data-ttu-id="662e0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="662e0-133">System.String</span></span>

## <span data-ttu-id="662e0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="662e0-134">OUTPUTS</span></span>

### <span data-ttu-id="662e0-135">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="662e0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="662e0-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="662e0-136">NOTES</span></span>

## <span data-ttu-id="662e0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="662e0-137">RELATED LINKS</span></span>
