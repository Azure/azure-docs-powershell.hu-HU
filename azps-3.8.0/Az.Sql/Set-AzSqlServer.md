---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845322"
---
# <span data-ttu-id="a4d11-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a4d11-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="a4d11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4d11-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d11-103">SQL-adatbázis kiszolgálójának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="a4d11-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="a4d11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4d11-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4d11-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d11-106">A **set-AzSqlServer** parancsmag egy Azure SQL-adatbázis kiszolgálójának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="a4d11-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="a4d11-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4d11-107">EXAMPLES</span></span>

### <span data-ttu-id="a4d11-108">1. példa: a rendszergazdai jelszó alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="a4d11-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="a4d11-109">Ez a parancs a server01 nevű AzureSQL-kiszolgálón visszaállítja a rendszergazdai jelszót.</span><span class="sxs-lookup"><span data-stu-id="a4d11-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="a4d11-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4d11-110">PARAMETERS</span></span>

### <span data-ttu-id="a4d11-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a4d11-111">-AssignIdentity</span></span>
<span data-ttu-id="a4d11-112">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="a4d11-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a4d11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d11-113">-DefaultProfile</span></span>
<span data-ttu-id="a4d11-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a4d11-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4d11-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4d11-115">-Force</span></span>
<span data-ttu-id="a4d11-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a4d11-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4d11-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a4d11-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="a4d11-118">Megadhatja, hogy engedélyezve van-e a hozzáférés, és hogy engedélyezve van-e a nyilvános hálózat elérésének engedélyezése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a4d11-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="a4d11-119">Ha le van tiltva, csak a privát hivatkozásokon keresztül elérhető kapcsolatok érhetik el ezt a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a4d11-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d11-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4d11-121">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="a4d11-121">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a4d11-122">-ServerName</span></span>
<span data-ttu-id="a4d11-123">Itt adhatja meg annak a kiszolgálónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a4d11-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a4d11-124">-ServerVersion</span></span>
<span data-ttu-id="a4d11-125">Annak a verziónak a verziószáma, amelyre a parancsmag a kiszolgálót módosítja.</span><span class="sxs-lookup"><span data-stu-id="a4d11-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="a4d11-126">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="a4d11-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="a4d11-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="a4d11-128">Új jelszót ad meg **SecureString** az adatbázis-kiszolgáló rendszergazdájához.</span><span class="sxs-lookup"><span data-stu-id="a4d11-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="a4d11-129">Ha **SecureString** szeretne beolvasni, használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4d11-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="a4d11-130">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a4d11-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

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

### <span data-ttu-id="a4d11-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a4d11-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="a4d11-132">Az SQL Server érvényesítéséhez szükséges minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="a4d11-132">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-133">-Címkék</span><span class="sxs-lookup"><span data-stu-id="a4d11-133">-Tags</span></span>
<span data-ttu-id="a4d11-134">A parancsmag által a kiszolgálóhoz társított címkék szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4d11-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="a4d11-135">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="a4d11-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="a4d11-136">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a4d11-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4d11-137">-Confirm</span></span>
<span data-ttu-id="a4d11-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4d11-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d11-139">-WhatIf</span></span>
<span data-ttu-id="a4d11-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4d11-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d11-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4d11-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d11-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d11-142">CommonParameters</span></span>
<span data-ttu-id="a4d11-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4d11-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d11-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4d11-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d11-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d11-145">INPUTS</span></span>

### <span data-ttu-id="a4d11-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d11-146">System.String</span></span>

## <span data-ttu-id="a4d11-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d11-147">OUTPUTS</span></span>

### <span data-ttu-id="a4d11-148">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a4d11-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a4d11-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4d11-149">NOTES</span></span>

## <span data-ttu-id="a4d11-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4d11-150">RELATED LINKS</span></span>

[<span data-ttu-id="a4d11-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a4d11-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
