---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366545"
---
# <span data-ttu-id="b24df-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="b24df-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="b24df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24df-102">SYNOPSIS</span></span>
<span data-ttu-id="b24df-103">Csak hibaelhárításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="b24df-103">Use for troubleshooting only.</span></span> <span data-ttu-id="b24df-104">Ez a parancs roll the storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="b24df-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="b24df-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b24df-105">SYNTAX</span></span>

### <span data-ttu-id="b24df-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b24df-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24df-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24df-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24df-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24df-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b24df-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b24df-109">DESCRIPTION</span></span>
<span data-ttu-id="b24df-110">Ez a parancs roll storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="b24df-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="b24df-111">Ezt hibaelhárítási esetekhez szánták.</span><span class="sxs-lookup"><span data-stu-id="b24df-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="b24df-112">A parancs hívásakor a kiszolgálói tanúsítványt lecseréli a rendszer, és frissíti a kiszolgáló által regisztrált tárterület-szinkronizálási szolgáltatást a kulcs nyilvános részének beküldével.</span><span class="sxs-lookup"><span data-stu-id="b24df-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="b24df-113">Mivel új tanúsítvány jön létre, a tanúsítvány lejárati ideje is frissül.</span><span class="sxs-lookup"><span data-stu-id="b24df-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="b24df-114">Ez a parancs a lejárt tanúsítványok frissítésére is használható.</span><span class="sxs-lookup"><span data-stu-id="b24df-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="b24df-115">Ez akkor fordulhat elő, ha egy kiszolgáló hosszabb ideig nem elérhető.</span><span class="sxs-lookup"><span data-stu-id="b24df-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="b24df-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b24df-116">EXAMPLES</span></span>

### <span data-ttu-id="b24df-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="b24df-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b24df-118">Ez a parancs a helyi kiszolgáló tanúsítványát roll roll and inform the corresponding storage sync service of the server's new identity, in a secure way.</span><span class="sxs-lookup"><span data-stu-id="b24df-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="b24df-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24df-119">PARAMETERS</span></span>

### <span data-ttu-id="b24df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24df-120">-DefaultProfile</span></span>
<span data-ttu-id="b24df-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b24df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24df-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b24df-122">-ParentObject</span></span>
<span data-ttu-id="b24df-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="b24df-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b24df-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b24df-124">-ParentResourceId</span></span>
<span data-ttu-id="b24df-125">StorageSyncService szülőerőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b24df-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b24df-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b24df-126">-PassThru</span></span>
<span data-ttu-id="b24df-127">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="b24df-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="b24df-128">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="b24df-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="b24df-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24df-129">-ResourceGroupName</span></span>
<span data-ttu-id="b24df-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b24df-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="b24df-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b24df-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="b24df-132">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="b24df-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b24df-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b24df-133">-Confirm</span></span>
<span data-ttu-id="b24df-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b24df-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b24df-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b24df-135">-WhatIf</span></span>
<span data-ttu-id="b24df-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b24df-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b24df-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b24df-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b24df-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24df-138">CommonParameters</span></span>
<span data-ttu-id="b24df-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24df-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24df-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24df-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24df-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b24df-141">INPUTS</span></span>

### <span data-ttu-id="b24df-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b24df-142">System.String</span></span>

### <span data-ttu-id="b24df-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b24df-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b24df-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b24df-144">OUTPUTS</span></span>

### <span data-ttu-id="b24df-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="b24df-145">System.Object</span></span>
## <span data-ttu-id="b24df-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b24df-146">NOTES</span></span>

## <span data-ttu-id="b24df-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b24df-147">RELATED LINKS</span></span>
