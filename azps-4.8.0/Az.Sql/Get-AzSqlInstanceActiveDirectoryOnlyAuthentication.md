---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183259"
---
# <span data-ttu-id="9318f-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9318f-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="9318f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9318f-102">SYNOPSIS</span></span>
<span data-ttu-id="9318f-103">Csak az Azure AD-hitelesítést kapja meg egy adott SQL-kezelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="9318f-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="9318f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9318f-104">SYNTAX</span></span>

### <span data-ttu-id="9318f-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9318f-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9318f-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9318f-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9318f-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9318f-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9318f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9318f-108">DESCRIPTION</span></span>
<span data-ttu-id="9318f-109">A **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag csak az Azure Active Directoryt (Azure ad) kapja meg az aktuális előfizetéshez tartozó AzureSQL kezelt példány hitelesítési követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="9318f-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="9318f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9318f-110">EXAMPLES</span></span>

### <span data-ttu-id="9318f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9318f-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="9318f-112">Ez a parancs csak az Azure Active Directoryt kapja meg (Azure AD) a ResourceGroup01 nevű ManagedInstance01 társított AzureSQL-beli felügyelt példány hitelesítési követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="9318f-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9318f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9318f-113">PARAMETERS</span></span>

### <span data-ttu-id="9318f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9318f-114">-DefaultProfile</span></span>
<span data-ttu-id="9318f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9318f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9318f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9318f-116">-InputObject</span></span>
<span data-ttu-id="9318f-117">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="9318f-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="9318f-118">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="9318f-118">-InstanceName</span></span>
<span data-ttu-id="9318f-119">Az Azure SQL által felügyelt példány neve, amelyre az Azure Active Directory csak a hitelesítés van bejelentkezve.</span><span class="sxs-lookup"><span data-stu-id="9318f-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="9318f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9318f-120">-ResourceGroupName</span></span>
<span data-ttu-id="9318f-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9318f-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="9318f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9318f-122">-ResourceId</span></span>
<span data-ttu-id="9318f-123">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9318f-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="9318f-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9318f-124">-Confirm</span></span>
<span data-ttu-id="9318f-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9318f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9318f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9318f-126">-WhatIf</span></span>
<span data-ttu-id="9318f-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9318f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9318f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9318f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9318f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9318f-129">CommonParameters</span></span>
<span data-ttu-id="9318f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9318f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9318f-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9318f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9318f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9318f-132">INPUTS</span></span>

### <span data-ttu-id="9318f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9318f-133">System.String</span></span>

## <span data-ttu-id="9318f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9318f-134">OUTPUTS</span></span>

### <span data-ttu-id="9318f-135">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="9318f-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="9318f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9318f-136">NOTES</span></span>

## <span data-ttu-id="9318f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9318f-137">RELATED LINKS</span></span>

[<span data-ttu-id="9318f-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9318f-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="9318f-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9318f-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="9318f-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9318f-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="9318f-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9318f-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

