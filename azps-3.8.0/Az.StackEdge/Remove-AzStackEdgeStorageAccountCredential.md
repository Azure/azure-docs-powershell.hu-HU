---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013907"
---
# <span data-ttu-id="49f27-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="49f27-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="49f27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49f27-102">SYNOPSIS</span></span>
<span data-ttu-id="49f27-103">Eltávolít egy eszköz tárolási fiókjának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="49f27-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="49f27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49f27-104">SYNTAX</span></span>

### <span data-ttu-id="49f27-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49f27-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49f27-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f27-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f27-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f27-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f27-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49f27-108">DESCRIPTION</span></span>
<span data-ttu-id="49f27-109">A **Remove-AzStackEdgeStorageAccountCredential** parancsmag eltávolítja a tárterület-fiók hitelesítő adatait a halom peremhálózati eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="49f27-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="49f27-110">Példák</span><span class="sxs-lookup"><span data-stu-id="49f27-110">EXAMPLES</span></span>

### <span data-ttu-id="49f27-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49f27-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="49f27-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49f27-112">PARAMETERS</span></span>

### <span data-ttu-id="49f27-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49f27-113">-AsJob</span></span>
<span data-ttu-id="49f27-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="49f27-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49f27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f27-115">-DefaultProfile</span></span>
<span data-ttu-id="49f27-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49f27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f27-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="49f27-117">-DeviceName</span></span>
<span data-ttu-id="49f27-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="49f27-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f27-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49f27-119">-InputObject</span></span>
<span data-ttu-id="49f27-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="49f27-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f27-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49f27-121">-Name</span></span>
<span data-ttu-id="49f27-122">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="49f27-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f27-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f27-123">-PassThru</span></span>
<span data-ttu-id="49f27-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="49f27-124">returns true if successful</span></span>

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

### <span data-ttu-id="49f27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f27-125">-ResourceGroupName</span></span>
<span data-ttu-id="49f27-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="49f27-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f27-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49f27-127">-ResourceId</span></span>
<span data-ttu-id="49f27-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="49f27-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f27-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49f27-129">-Confirm</span></span>
<span data-ttu-id="49f27-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49f27-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f27-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f27-131">-WhatIf</span></span>
<span data-ttu-id="49f27-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49f27-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49f27-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49f27-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f27-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f27-134">CommonParameters</span></span>
<span data-ttu-id="49f27-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49f27-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f27-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49f27-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f27-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f27-137">INPUTS</span></span>

### <span data-ttu-id="49f27-138">System. String</span><span class="sxs-lookup"><span data-stu-id="49f27-138">System.String</span></span>

### <span data-ttu-id="49f27-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="49f27-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="49f27-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f27-140">OUTPUTS</span></span>

### <span data-ttu-id="49f27-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49f27-141">System.Boolean</span></span>

## <span data-ttu-id="49f27-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49f27-142">NOTES</span></span>

## <span data-ttu-id="49f27-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49f27-143">RELATED LINKS</span></span>
