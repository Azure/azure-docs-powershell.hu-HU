---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182092"
---
# <span data-ttu-id="ff39e-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="ff39e-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="ff39e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff39e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff39e-103">A virtuális virtuálisgép-konfigurációban egy SQL-virtuálisgép-csoporthoz viszonyított információt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff39e-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="ff39e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff39e-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff39e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff39e-105">DESCRIPTION</span></span>
<span data-ttu-id="ff39e-106">A Set-AzSqlVMConfigGroup parancsmag a virtuális virtuálisgép-konfiguráció SQL-virtuálisgép-csoportjához való csatlakozáshoz szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff39e-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="ff39e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff39e-107">EXAMPLES</span></span>

### <span data-ttu-id="ff39e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff39e-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="ff39e-109">Az SQL virtuálisgép-konfiguráció csoport-információinak frissítése</span><span class="sxs-lookup"><span data-stu-id="ff39e-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="ff39e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff39e-110">PARAMETERS</span></span>

### <span data-ttu-id="ff39e-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="ff39e-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="ff39e-112">A fürt bootstrap fiókjának jelszava</span><span class="sxs-lookup"><span data-stu-id="ff39e-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="ff39e-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="ff39e-114">A cluster Operator fiók jelszava</span><span class="sxs-lookup"><span data-stu-id="ff39e-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="ff39e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff39e-115">-DefaultProfile</span></span>
<span data-ttu-id="ff39e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff39e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff39e-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="ff39e-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="ff39e-118">Az SQL-szolgáltatásfiók jelszava</span><span class="sxs-lookup"><span data-stu-id="ff39e-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="ff39e-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="ff39e-119">-SqlVM</span></span>
<span data-ttu-id="ff39e-120">Az SQL virtuálisgép-konfiguráció, amelyre a csoporttagság hozzáadódik</span><span class="sxs-lookup"><span data-stu-id="ff39e-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ff39e-121">-SqlVMGroup</span></span>
<span data-ttu-id="ff39e-122">Az SQL Virtual Machine csoport része lesz</span><span class="sxs-lookup"><span data-stu-id="ff39e-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff39e-123">CommonParameters</span></span>
<span data-ttu-id="ff39e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff39e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff39e-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ff39e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff39e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39e-126">INPUTS</span></span>

### <span data-ttu-id="ff39e-127">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ff39e-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ff39e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39e-128">OUTPUTS</span></span>

### <span data-ttu-id="ff39e-129">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ff39e-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ff39e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff39e-130">NOTES</span></span>

## <span data-ttu-id="ff39e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff39e-131">RELATED LINKS</span></span>
