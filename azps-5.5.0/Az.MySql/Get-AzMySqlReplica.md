---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147330"
---
# <span data-ttu-id="0480e-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="0480e-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="0480e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0480e-102">SYNOPSIS</span></span>
<span data-ttu-id="0480e-103">List all the replika for a given server.</span><span class="sxs-lookup"><span data-stu-id="0480e-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0480e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0480e-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0480e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0480e-105">DESCRIPTION</span></span>
<span data-ttu-id="0480e-106">List all the replika for a given server.</span><span class="sxs-lookup"><span data-stu-id="0480e-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0480e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0480e-107">EXAMPLES</span></span>

### <span data-ttu-id="0480e-108">1. példa: A MySql-kiszolgálói replika lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="0480e-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0480e-109">Ez a parancsmag a MySql-kiszolgálói replikát erőforráscsoport és kiszolgálónév alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0480e-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="0480e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0480e-110">PARAMETERS</span></span>

### <span data-ttu-id="0480e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0480e-111">-DefaultProfile</span></span>
<span data-ttu-id="0480e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0480e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0480e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0480e-113">-ResourceGroupName</span></span>
<span data-ttu-id="0480e-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0480e-114">The name of the resource group.</span></span>
<span data-ttu-id="0480e-115">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0480e-115">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0480e-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0480e-116">-ServerName</span></span>
<span data-ttu-id="0480e-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0480e-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0480e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0480e-118">-SubscriptionId</span></span>
<span data-ttu-id="0480e-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0480e-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0480e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0480e-120">CommonParameters</span></span>
<span data-ttu-id="0480e-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0480e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0480e-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0480e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0480e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0480e-123">INPUTS</span></span>

## <span data-ttu-id="0480e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0480e-124">OUTPUTS</span></span>

### <span data-ttu-id="0480e-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="0480e-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0480e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0480e-126">NOTES</span></span>

<span data-ttu-id="0480e-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0480e-127">ALIASES</span></span>

## <span data-ttu-id="0480e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0480e-128">RELATED LINKS</span></span>

