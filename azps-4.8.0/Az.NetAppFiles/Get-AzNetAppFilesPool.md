---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 257421a43c3da11c82316eaf58d2983fe47d5f05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024671"
---
# <span data-ttu-id="6d4aa-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6d4aa-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6d4aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4aa-103">Információt kap az Azure NetApp-fájlok (ANF) készletéből.</span><span class="sxs-lookup"><span data-stu-id="6d4aa-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6d4aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d4aa-104">SYNTAX</span></span>

### <span data-ttu-id="6d4aa-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d4aa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d4aa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d4aa-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d4aa-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d4aa-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d4aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d4aa-108">DESCRIPTION</span></span>
<span data-ttu-id="6d4aa-109">A **Get-AzNetAppFilesPool** PARANCSMAG egy ANF-készlet adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d4aa-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="6d4aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6d4aa-110">EXAMPLES</span></span>

### <span data-ttu-id="6d4aa-111">Példa 1: ANF-készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d4aa-111">Example 1: Get an ANF pool</span></span>
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
ProvisioningState : Succeeded
```

<span data-ttu-id="6d4aa-112">Ez a parancs a MyAnfPool nevű fiókot a "MyAnfAccount" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d4aa-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="6d4aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d4aa-113">PARAMETERS</span></span>

### <span data-ttu-id="6d4aa-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d4aa-114">-AccountName</span></span>
<span data-ttu-id="6d4aa-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="6d4aa-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="6d4aa-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d4aa-116">-AccountObject</span></span>
<span data-ttu-id="6d4aa-117">A visszaadni kívánt készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="6d4aa-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="6d4aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4aa-118">-DefaultProfile</span></span>
<span data-ttu-id="6d4aa-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d4aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d4aa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d4aa-120">-Name</span></span>
<span data-ttu-id="6d4aa-121">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="6d4aa-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6d4aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d4aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d4aa-123">A ANF-készlet erőforráscsoport csoportja</span><span class="sxs-lookup"><span data-stu-id="6d4aa-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="6d4aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d4aa-124">-ResourceId</span></span>
<span data-ttu-id="6d4aa-125">A ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6d4aa-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="6d4aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4aa-126">CommonParameters</span></span>
<span data-ttu-id="6d4aa-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d4aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4aa-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d4aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4aa-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d4aa-129">INPUTS</span></span>

### <span data-ttu-id="6d4aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d4aa-130">System.String</span></span>

### <span data-ttu-id="6d4aa-131">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6d4aa-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6d4aa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d4aa-132">OUTPUTS</span></span>

### <span data-ttu-id="6d4aa-133">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6d4aa-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6d4aa-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d4aa-134">NOTES</span></span>

## <span data-ttu-id="6d4aa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d4aa-135">RELATED LINKS</span></span>
