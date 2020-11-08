---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188167"
---
# <span data-ttu-id="719cc-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="719cc-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="719cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="719cc-102">SYNOPSIS</span></span>
<span data-ttu-id="719cc-103">Letiltja az Azure AD only hitelesítést egy bizonyos SQL-kezelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="719cc-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="719cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="719cc-104">SYNTAX</span></span>

### <span data-ttu-id="719cc-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="719cc-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719cc-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="719cc-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719cc-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="719cc-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="719cc-108">DESCRIPTION</span></span>
<span data-ttu-id="719cc-109">A **disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag letiltja az Azure Active Directoryt (Azure ad), ha az aktuális előfizetésben csak a AzureSQL kezelt példány hitelesítési követelményeire van szükség.</span><span class="sxs-lookup"><span data-stu-id="719cc-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="719cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="719cc-110">EXAMPLES</span></span>

### <span data-ttu-id="719cc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="719cc-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="719cc-112">Ez a parancs letiltja az Azure Active Directoryt (Azure AD) csak a ResourceGroup01 nevű ManagedInstance01 társított AzureSQL-alapú felügyelt példány hitelesítési követelményét.</span><span class="sxs-lookup"><span data-stu-id="719cc-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="719cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="719cc-113">PARAMETERS</span></span>

### <span data-ttu-id="719cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719cc-114">-DefaultProfile</span></span>
<span data-ttu-id="719cc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="719cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="719cc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="719cc-116">-InputObject</span></span>
<span data-ttu-id="719cc-117">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="719cc-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="719cc-118">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="719cc-118">-InstanceName</span></span>
<span data-ttu-id="719cc-119">Az Azure SQL által felügyelt példány neve, amelyre az Azure Active Directory csak a hitelesítés van bejelentkezve.</span><span class="sxs-lookup"><span data-stu-id="719cc-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="719cc-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="719cc-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="719cc-122">-ResourceId</span></span>
<span data-ttu-id="719cc-123">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="719cc-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cc-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="719cc-124">-Confirm</span></span>
<span data-ttu-id="719cc-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="719cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719cc-126">-WhatIf</span></span>
<span data-ttu-id="719cc-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="719cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719cc-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="719cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719cc-129">CommonParameters</span></span>
<span data-ttu-id="719cc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="719cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719cc-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="719cc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719cc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="719cc-132">INPUTS</span></span>

### <span data-ttu-id="719cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="719cc-133">System.String</span></span>

## <span data-ttu-id="719cc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="719cc-134">OUTPUTS</span></span>

### <span data-ttu-id="719cc-135">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="719cc-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="719cc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="719cc-136">NOTES</span></span>

## <span data-ttu-id="719cc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="719cc-137">RELATED LINKS</span></span>

[<span data-ttu-id="719cc-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="719cc-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="719cc-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="719cc-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="719cc-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="719cc-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="719cc-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="719cc-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)