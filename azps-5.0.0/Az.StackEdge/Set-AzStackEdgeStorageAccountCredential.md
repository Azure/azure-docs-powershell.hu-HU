---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187198"
---
# <span data-ttu-id="aee7f-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aee7f-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aee7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aee7f-102">SYNOPSIS</span></span>
<span data-ttu-id="aee7f-103">Beállítja egy eszköz tárolási fiókjának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="aee7f-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="aee7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aee7f-104">SYNTAX</span></span>

### <span data-ttu-id="aee7f-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aee7f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee7f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee7f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aee7f-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee7f-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee7f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aee7f-108">DESCRIPTION</span></span>
<span data-ttu-id="aee7f-109">A **set-AzStackEdgeStorageAccountCredential** parancsmag a halom szélén lévő eszköz tárolási fiókjához tartozó tárolási fiók hitelesítő adatait frissíti.</span><span class="sxs-lookup"><span data-stu-id="aee7f-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="aee7f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aee7f-110">EXAMPLES</span></span>

### <span data-ttu-id="aee7f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aee7f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="aee7f-112">Segítséget nyújt a tárolási fiókok elérési kulcsainak elforgatásához</span><span class="sxs-lookup"><span data-stu-id="aee7f-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="aee7f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aee7f-113">PARAMETERS</span></span>

### <span data-ttu-id="aee7f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aee7f-114">-AsJob</span></span>
<span data-ttu-id="aee7f-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aee7f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aee7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee7f-116">-DefaultProfile</span></span>
<span data-ttu-id="aee7f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aee7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee7f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aee7f-118">-DeviceName</span></span>
<span data-ttu-id="aee7f-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="aee7f-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aee7f-120">-EncryptionKey</span></span>
<span data-ttu-id="aee7f-121">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="aee7f-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aee7f-122">-InputObject</span></span>
<span data-ttu-id="aee7f-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="aee7f-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aee7f-124">-Name</span></span>
<span data-ttu-id="aee7f-125">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="aee7f-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee7f-126">-ResourceGroupName</span></span>
<span data-ttu-id="aee7f-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="aee7f-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aee7f-128">-ResourceId</span></span>
<span data-ttu-id="aee7f-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="aee7f-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="aee7f-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="aee7f-131">tárolási fiók elérési kulcsának biztosítása</span><span class="sxs-lookup"><span data-stu-id="aee7f-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee7f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aee7f-132">-Confirm</span></span>
<span data-ttu-id="aee7f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aee7f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee7f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee7f-134">-WhatIf</span></span>
<span data-ttu-id="aee7f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aee7f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aee7f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aee7f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee7f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee7f-137">CommonParameters</span></span>
<span data-ttu-id="aee7f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aee7f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee7f-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aee7f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee7f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aee7f-140">INPUTS</span></span>

### <span data-ttu-id="aee7f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aee7f-141">System.String</span></span>

### <span data-ttu-id="aee7f-142">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aee7f-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aee7f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aee7f-143">OUTPUTS</span></span>

### <span data-ttu-id="aee7f-144">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aee7f-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aee7f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aee7f-145">NOTES</span></span>

## <span data-ttu-id="aee7f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aee7f-146">RELATED LINKS</span></span>