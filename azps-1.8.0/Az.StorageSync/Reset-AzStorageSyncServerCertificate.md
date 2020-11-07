---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668472"
---
# <span data-ttu-id="59600-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="59600-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="59600-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59600-102">SYNOPSIS</span></span>
<span data-ttu-id="59600-103">Csak hibaelhárítás esetén használható.</span><span class="sxs-lookup"><span data-stu-id="59600-103">Use for troubleshooting only.</span></span> <span data-ttu-id="59600-104">Ez a parancs a tárterület-szinkronizálási kiszolgáló tanúsítványát fogja használni a kiszolgáló identitásának a tárterület-szinkronizálási szolgáltatáshoz való leírásához.</span><span class="sxs-lookup"><span data-stu-id="59600-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="59600-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59600-105">SYNTAX</span></span>

### <span data-ttu-id="59600-106">ObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59600-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59600-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="59600-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59600-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="59600-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59600-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="59600-109">DESCRIPTION</span></span>
<span data-ttu-id="59600-110">Ez a parancs a tárterület-szinkronizáló kiszolgáló tanúsítványát használja a kiszolgáló identitásának a tárterület-szinkronizálási szolgáltatáshoz való leírásához.</span><span class="sxs-lookup"><span data-stu-id="59600-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="59600-111">Ez a funkció azt jelenti, hogy a hibaelhárítási helyzetekben kell használni.</span><span class="sxs-lookup"><span data-stu-id="59600-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="59600-112">A parancs hívásakor a rendszer lecseréli a kiszolgáló tanúsítványát, és frissíti a tárterület-szinkronizálási szolgáltatást, és a kulcs nyilvános részét beküldi a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="59600-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="59600-113">Az új tanúsítvány létrehozása óta a tanúsítvány elévülési ideje is frissül.</span><span class="sxs-lookup"><span data-stu-id="59600-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="59600-114">Ezt a parancsot a lejárt tanúsítványok frissítésére is használhatja.</span><span class="sxs-lookup"><span data-stu-id="59600-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="59600-115">Ez akkor fordulhat elő, ha egy kiszolgáló hosszabb ideig kapcsolat nélküli üzemmódban van.</span><span class="sxs-lookup"><span data-stu-id="59600-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="59600-116">Példák</span><span class="sxs-lookup"><span data-stu-id="59600-116">EXAMPLES</span></span>

### <span data-ttu-id="59600-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59600-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="59600-118">Ez a parancs a helyi kiszolgáló tanúsítványát fogja legörgetni, és biztonságos módon tájékoztatja a kiszolgáló új identitásának megfelelő tárterület-szinkronizálási szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="59600-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="59600-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59600-119">PARAMETERS</span></span>

### <span data-ttu-id="59600-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59600-120">-DefaultProfile</span></span>
<span data-ttu-id="59600-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59600-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59600-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="59600-122">-ParentObject</span></span>
<span data-ttu-id="59600-123">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="59600-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59600-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59600-124">-ParentResourceId</span></span>
<span data-ttu-id="59600-125">A StorageSyncService szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="59600-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59600-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59600-126">-PassThru</span></span>
<span data-ttu-id="59600-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="59600-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="59600-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59600-128">-ResourceGroupName</span></span>
<span data-ttu-id="59600-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="59600-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59600-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="59600-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="59600-131">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="59600-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59600-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59600-132">-Confirm</span></span>
<span data-ttu-id="59600-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59600-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59600-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59600-134">-WhatIf</span></span>
<span data-ttu-id="59600-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59600-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59600-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59600-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59600-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59600-137">CommonParameters</span></span>
<span data-ttu-id="59600-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59600-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59600-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59600-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59600-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59600-140">INPUTS</span></span>

### <span data-ttu-id="59600-141">System. String</span><span class="sxs-lookup"><span data-stu-id="59600-141">System.String</span></span>

### <span data-ttu-id="59600-142">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="59600-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="59600-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59600-143">OUTPUTS</span></span>

### <span data-ttu-id="59600-144">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="59600-144">System.Object</span></span>
## <span data-ttu-id="59600-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59600-145">NOTES</span></span>

## <span data-ttu-id="59600-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59600-146">RELATED LINKS</span></span>
