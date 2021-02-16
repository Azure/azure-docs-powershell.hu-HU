---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404173"
---
# <span data-ttu-id="195ab-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="195ab-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="195ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195ab-102">SYNOPSIS</span></span>
<span data-ttu-id="195ab-103">Kiszolgálókapcsolat környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="195ab-103">Creates a server connection context.</span></span>

## <span data-ttu-id="195ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="195ab-104">SYNTAX</span></span>

### <span data-ttu-id="195ab-105">ByServerNameWithSqlAuth (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="195ab-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="195ab-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="195ab-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="195ab-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="195ab-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="195ab-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="195ab-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="195ab-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="195ab-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="195ab-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="195ab-110">DESCRIPTION</span></span>
<span data-ttu-id="195ab-111">A **New-AzureSqlDatabaseServerContext** parancsmag létrehoz egy Azure SQL Database Server-kapcsolatkörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="195ab-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="195ab-112">Az SQL Server-hitelesítéssel kapcsolatot hozhat létre egy SQL-adatbázis-kiszolgálóval a megadott hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="195ab-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="195ab-113">Az SQL-adatbázis-kiszolgálót név, teljes név vagy URL-cím szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="195ab-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="195ab-114">Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot, amely a felhasználónév és a jelszó megadására kéri.</span><span class="sxs-lookup"><span data-stu-id="195ab-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="195ab-115">A **New-AzureSqlDatabaseServerContext** parancsmag tanúsítványalapú hitelesítéssel való használatával kapcsolatot hozhat létre a megadott SQL Database-kiszolgálóval a megadott Azure-előfizetési adatok használatával.</span><span class="sxs-lookup"><span data-stu-id="195ab-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="195ab-116">Az SQL-adatbázis kiszolgálóját név vagy teljesen minősített név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="195ab-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="195ab-117">Az előfizetés adatait megadhatja paraméterként, vagy lekérheti az aktuális Azure-előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="195ab-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="195ab-118">Az aktuális Azure-előfizetés kiválasztásához használja a https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Select-AzureSubscription parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="195ab-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="195ab-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="195ab-119">EXAMPLES</span></span>

### <span data-ttu-id="195ab-120">1. példa: Környezet létrehozása SQL Server-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="195ab-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="195ab-121">Ez a példa SQL Server-hitelesítést használ.</span><span class="sxs-lookup"><span data-stu-id="195ab-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="195ab-122">Az első parancs a kiszolgáló rendszergazdájának hitelesítő adatait kéri, és a hitelesítő adatokat a $Credential tárolja.</span><span class="sxs-lookup"><span data-stu-id="195ab-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="195ab-123">A második parancs az lpqd0zbr8y nevű SQL Database-kiszolgálóhoz csatlakozik az $Credential.</span><span class="sxs-lookup"><span data-stu-id="195ab-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="195ab-124">Az utolsó parancs létrehoz egy Adatbázis17 nevű adatbázist a kiszolgálón, amely a helyi környezet $Context.</span><span class="sxs-lookup"><span data-stu-id="195ab-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="195ab-125">2. példa: Környezet létrehozása tanúsítványalapú hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="195ab-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="195ab-126">Ez a példa a tanúsítványalapú hitelesítést használja.</span><span class="sxs-lookup"><span data-stu-id="195ab-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="195ab-127">Az első két parancs értékeket rendel a $SubscriptionId és $Thumbprint változókhoz.</span><span class="sxs-lookup"><span data-stu-id="195ab-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="195ab-128">A harmadik parancs a tanúsítványt a $Thumbprint azonosítja, és $Certificate.</span><span class="sxs-lookup"><span data-stu-id="195ab-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="195ab-129">A negyedik parancs az előfizetést Előfizetés07-re állítja, az ötödik parancs pedig az előfizetést választja ki.</span><span class="sxs-lookup"><span data-stu-id="195ab-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="195ab-130">Az utolsó parancs létrehoz egy kontextust az aktuális előfizetésben az lpqd0zbr8y nevű kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="195ab-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="195ab-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="195ab-131">PARAMETERS</span></span>

### <span data-ttu-id="195ab-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="195ab-132">-Credential</span></span>
<span data-ttu-id="195ab-133">Egy hitelesítőadat-objektumot ad meg, amely SQL Server-hitelesítést biztosít a kiszolgáló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="195ab-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="195ab-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="195ab-135">Az Azure SQL-adatbázis kiszolgálójának teljes tartománynevét (FQDN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="195ab-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="195ab-136">Például: Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="195ab-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="195ab-137">-ManageUrl</span></span>
<span data-ttu-id="195ab-138">A parancsmag által a kiszolgáló Azure SQL DatabaseManagement Portáljának eléréséhez használt URL-cím.</span><span class="sxs-lookup"><span data-stu-id="195ab-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="195ab-139">-Profile</span></span>
<span data-ttu-id="195ab-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="195ab-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="195ab-141">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="195ab-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="195ab-142">-ServerName</span></span>
<span data-ttu-id="195ab-143">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="195ab-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="195ab-144">-SubscriptionName</span></span>
<span data-ttu-id="195ab-145">Megadja annak az Azure-előfizetésnek a nevét, amelyből a parancsmag létrehozza a kapcsolat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="195ab-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="195ab-146">Ha nem ad meg értéket ehhez a paraméterhez, a parancsmag az aktuális előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="195ab-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="195ab-147">Az aktuális előfizetés Select-AzureSubscription a Select-AzureSubscription parancsmag futtatásával.</span><span class="sxs-lookup"><span data-stu-id="195ab-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="195ab-148">-UseSubscription</span></span>
<span data-ttu-id="195ab-149">Azt jelzi, hogy ez a parancsmag Azure-előfizetést használ a kapcsolat környezetének létrehozására.</span><span class="sxs-lookup"><span data-stu-id="195ab-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195ab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195ab-150">CommonParameters</span></span>
<span data-ttu-id="195ab-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195ab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195ab-152">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195ab-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195ab-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="195ab-153">INPUTS</span></span>

## <span data-ttu-id="195ab-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="195ab-154">OUTPUTS</span></span>

### <span data-ttu-id="195ab-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="195ab-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="195ab-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="195ab-156">NOTES</span></span>
* <span data-ttu-id="195ab-157">Ha tartomány megadása nélkül hitelesít, és Windows PowerShell 2.0-t használ, a Get-Credential-parancsmag egy, a felhasználónévhez előrendelt törtjelet () ad vissza, például \\ \user.</span><span class="sxs-lookup"><span data-stu-id="195ab-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="195ab-158">A Windows PowerShell 3.0 nem adja hozzá a perjelet.</span><span class="sxs-lookup"><span data-stu-id="195ab-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="195ab-159">A törtjelet nem ismeri  fel a **New-AzureSqlDatabaseServerContext** parancsmag hitelesítőadat-paramétere.</span><span class="sxs-lookup"><span data-stu-id="195ab-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="195ab-160">Az eltávolításához az alábbihoz hasonló parancsokat kell használnia:</span><span class="sxs-lookup"><span data-stu-id="195ab-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="195ab-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="195ab-161">RELATED LINKS</span></span>



[<span data-ttu-id="195ab-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="195ab-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="195ab-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="195ab-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="195ab-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="195ab-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="195ab-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="195ab-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


