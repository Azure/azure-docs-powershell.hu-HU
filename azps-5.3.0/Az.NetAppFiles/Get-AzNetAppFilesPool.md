---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466271"
---
# <span data-ttu-id="df4f8-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="df4f8-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="df4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="df4f8-103">Az Azure NetApp-fájlok (ANF) készlet részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="df4f8-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="df4f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df4f8-104">SYNTAX</span></span>

### <span data-ttu-id="df4f8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df4f8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4f8-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4f8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4f8-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df4f8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df4f8-108">DESCRIPTION</span></span>
<span data-ttu-id="df4f8-109">A **Get-AzNetAppFilesPool** parancsmag egy ANF-készlet adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="df4f8-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="df4f8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df4f8-110">EXAMPLES</span></span>

### <span data-ttu-id="df4f8-111">1. példa: ANF-készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="df4f8-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="df4f8-112">Ez a parancs a MyAnfPool nevű fiókot a "MyAnfAccount" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="df4f8-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="df4f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df4f8-113">PARAMETERS</span></span>

### <span data-ttu-id="df4f8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df4f8-114">-AccountName</span></span>
<span data-ttu-id="df4f8-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="df4f8-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4f8-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="df4f8-116">-AccountObject</span></span>
<span data-ttu-id="df4f8-117">A vissza nem térhet készletet tartalmazó fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="df4f8-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4f8-118">-DefaultProfile</span></span>
<span data-ttu-id="df4f8-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df4f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df4f8-120">-Name</span></span>
<span data-ttu-id="df4f8-121">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="df4f8-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="df4f8-123">Az ANF-készlet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="df4f8-123">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4f8-124">-ResourceId</span></span>
<span data-ttu-id="df4f8-125">Az ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="df4f8-125">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4f8-126">CommonParameters</span></span>
<span data-ttu-id="df4f8-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4f8-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df4f8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4f8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df4f8-129">INPUTS</span></span>

### <span data-ttu-id="df4f8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df4f8-130">System.String</span></span>

### <span data-ttu-id="df4f8-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="df4f8-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="df4f8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4f8-132">OUTPUTS</span></span>

### <span data-ttu-id="df4f8-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="df4f8-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="df4f8-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df4f8-134">NOTES</span></span>

## <span data-ttu-id="df4f8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df4f8-135">RELATED LINKS</span></span>
